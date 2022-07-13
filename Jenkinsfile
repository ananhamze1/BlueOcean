pipeline {
  agent any
  stages {
    stage('s') {
      post {
        success {
          sh 'echo 1'
        }

        failure {
          sh 'echo 2'
        }

      }
      steps {
        sh 'echo 1'
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