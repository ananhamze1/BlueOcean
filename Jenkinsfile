pipeline {
  agent any
  stages {
    stage('Clone') {
      steps {
        dir(path: '/home/shr_mibuilder/Desktop/equivalence') {
          git(url: 'git@gitlab-gxp.cloud.health.ge.com:NMSW/nuca_falcon.git', branch: 'staging')
        }

      }
    }

  }
  environment {
    TEMP_DIR = '/home/shr_mibuilder/Desktop/equivalence'
  }
}