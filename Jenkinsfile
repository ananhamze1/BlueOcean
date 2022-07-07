pipeline {
  agent any
  stages {
    stage('error') {
      steps {
        sh '''cd /home/shr_mibuilder/Desktop
setnev TABLE 1
$TABLE=`cat table`'''
      }
    }

  }
  options {
    skipDefaultCheckout()
  }
}