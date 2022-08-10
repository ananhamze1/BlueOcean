pipeline {
  agent any
  stages {
    stage('Clone') {
      steps {
        dir(path: '$TEMP_DIR') {
          git(url: 'git@gitlab-gxp.cloud.health.ge.com:MI-DEVOPS/NGC.git', branch: 'devops')
        }

      }
    }

  }
  environment {
    TEMP_DIR = '/home/shr_mibuilder/Desktop/equivalence'
  }
}