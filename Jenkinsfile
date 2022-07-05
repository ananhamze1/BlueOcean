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
        sh 'echo "${BUILD_USER_FIRST_NAME}"'
      }
    }

  }
}