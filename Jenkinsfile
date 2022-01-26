pipeline {
  agent any
  stages {
    stage('first') {
      steps {
        echo '1'
      }
    }

    stage('second') {
      steps {
        echo '2'
      }
    }

    stage('third') {
      steps {
        echo '3'
      }
    }

    stage('fourth') {
      steps {
        echo '4'
      }
    }

  }
  environment {
    http_proxy = 'http://PITC-Zscaler-EMEA-Amsterdam3PR.proxy.corporate.gdn.ge.com:80/'
    https_proxy = 'http://PITC-Zscaler-EMEA-Amsterdam3PR.proxy.corporate.gdn.ge.com:80/'
  }
}