pipeline {
  agent any
  stages {
    stage('123') {
      steps {
        echo '1'
      }
    }

    stage('a') {
      steps {
        catchError(buildResult: 'SUCCESS', stageResult: 'SUCCESS') {
          sh 'exit 1'
        }

      }
    }

  }
}