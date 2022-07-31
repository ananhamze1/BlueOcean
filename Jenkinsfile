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
        catchError(buildResult: 'FAILURE', stageResult: 'FAILURE') {
          sh 'exit 1'
        }

      }
    }

  }
}