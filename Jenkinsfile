pipeline {
  agent any
  stages {
    stage('s') {
      post {
        always {
          sh 'echo $stageResult'
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