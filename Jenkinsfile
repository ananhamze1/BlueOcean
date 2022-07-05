pipeline {
  agent any
  stages {
    stage('build user') {
      steps {
        wrap(delegate: [$class: 'BuildUser']) {
          sh 'echo "${BUILD_USER}"'
        }

      }
    }

  }
  options {
    skipDefaultCheckout()
  }
}