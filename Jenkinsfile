pipeline {
  agent any
  stages {
    stage('ss') {
      steps {
        sh 'git clone --branch staging git@gitlab-gxp.cloud.health.ge.com:NMSW/nuca_falcon.git'
      }
    }

  }
  environment {
    TEMP_DIR = '/home/shr_mibuilder/Desktop/equivalence'
  }
}