pipeline {
  agent any
  stages {
    stage('s') {
      post {
        success {
          sh 'echo 2'
        }

        failure {
          sh 'echo 1'
        }

      }
      steps {
        sh 'exit 1'
      }
    }

    stage('error') {
      steps {
        sh 'echo $stageResult'
      }
    }

  }
  options {
    skipDefaultCheckout()
  }
}