pipeline {
  agent any
  stages {
    stage('first') {
      steps {
        catchError(buildResult: 'success', message: '123', stageResult: 'failure') {
          sh 'exit 1'
        }

        script {
          STAGE="$STAGE_RESULT"
          echo '1'
        }

      }
    }

    stage('123') {
      steps {
        echo '123'
        echo "$STAGE"
      }
    }

  }
  environment {
    http_proxy = 'http://PITC-Zscaler-EMEA-Amsterdam3PR.proxy.corporate.gdn.ge.com:80/'
    https_proxy = 'http://PITC-Zscaler-EMEA-Amsterdam3PR.proxy.corporate.gdn.ge.com:80/'
  }
}