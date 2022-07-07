pipeline {
  agent any
  stages {
    stage('Create RPMs and ISO') {
      steps {
        sh '''cd /home/shr_mibuilder/Desktop
export TABLE=1'''
        script {
          TABLE = 'cat html'
        }

        sh 'echo $TABLE'
      }
    }

  }
  options {
    skipDefaultCheckout()
  }
}