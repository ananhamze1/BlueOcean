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
        echo '${BUILD_USER}'
      }
    }

  }
}