pipeline {
  agent any
  stages {
    stage('1') {
      steps {
        echo '3'
      }
    }

    stage('3') {
      steps {
        sh 'echo ${env.BUILD_NUMBER}'
      }
    }

  }
  post {
    always {
      script {
        emailext body: "OS: HELIOS<br> NGC Jenkins Build ${currentBuild.result}, build number ${env.BUILD_NUMBER}<br> More info at: http://10.135.193.70:8080/blue/organizations/jenkins/NGC1%2FNGC_Build/detail/NGC_Build/${env.BUILD_NUMBER}/pipeline<br> NGC Automation:  <br> Embedded Coverity:  <br> Java Coverity:<br> CPP Coverity: ",
        to: "rawad.khalaila@ge.com",
        subject: "${currentBuild.result} NGC Jenkins Build"
      }

    }

  }
}