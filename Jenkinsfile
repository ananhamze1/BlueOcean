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
        sh 'echo $stageResult'
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