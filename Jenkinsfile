pipeline {
  agent any
  stages {
    stage('first') {
      steps {
        script {
          STAGE="failure"
          echo '1'
        }

        catchError(buildResult: 'success', message: '123', stageResult: 'failure', catchInterruptions: true) {
          sh 'exit 0'
          script {
            STAGE="success"
            echo '2'
          }

        }

      }
    }

    stage('123') {
      steps {
        echo '3'
        echo "$STAGE"
      }
    }

  }
  environment {
    http_proxy = 'http://PITC-Zscaler-EMEA-Amsterdam3PR.proxy.corporate.gdn.ge.com:80/'
    https_proxy = 'http://PITC-Zscaler-EMEA-Amsterdam3PR.proxy.corporate.gdn.ge.com:80/'
  }
}