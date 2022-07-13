pipeline {
  agent any
  stages {
    stage('s') {
      steps {
        sh 'echo $stageResult'
      }
    }

  }
  options {
    skipDefaultCheckout()
  }
}