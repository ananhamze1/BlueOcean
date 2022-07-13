pipeline {
  agent any
  stages {
    stage('s') {
      steps {
        sh 'echo $STAGE_NAME'
      }
    }

  }
  options {
    skipDefaultCheckout()
  }
}