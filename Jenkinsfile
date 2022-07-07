pipeline {
  agent any
  stages {
    stage('s') {
      steps {
        sh '''cd /home/shr_mibuilder/Desktop
export TABLE=\'cat table\'
echo $TABLE'''
      }
    }

  }
  options {
    skipDefaultCheckout()
  }
}