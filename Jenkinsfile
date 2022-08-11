pipeline {
  agent any
  stages {
    stage('Clone') {
      steps {
        sh 'mkdir /home/shr_mibuilder/Desktop/dir'
        dir(path: '$TEMP_DIR') {
          git(url: 'git@gitlab-gxp.cloud.health.ge.com:NMSW/nuca_falcon.git', branch: 'staging')
        }

      }
    }

  }
  environment {
    TEMP_DIR = '/home/shr_mibuilder/Desktop/equivalence'
  }
}