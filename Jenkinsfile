pipeline {
  agent any
  stages {
    stage('Create RPMs and ISO') {
      steps {
        sh '''cd /home/shr_mibuilder/Desktop
setenv TABLE 1'''
        script {
          TABLE = '2'
        }

      }
    }

  }
  options {
    skipDefaultCheckout()
  }
}