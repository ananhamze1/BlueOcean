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
        echo 'a'
      }
    }

  }
  post {
    always {
      script {
        emailext body: "${currentBuild.result}",
        to: "rawad.khalaila@ge.com",
        subject: "${currentBuild.result} NGC Jenkins Build"
      }

    }

  }
}