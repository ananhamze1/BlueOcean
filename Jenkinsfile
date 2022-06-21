pipeline {
  agent any
  stages {
    stage('1') {
      steps {
        echo '3'
      }
    }

    stage('2') {
      steps {
        catchError(buildResult: 'FAILURE', stageResult: 'FAILURE') {
          sh '''su ctuser -c "echo 1"
'''
        }

      }
    }

    stage('3') {
      steps {
        echo 'a'
      }
    }

  }
  environment {
    http_proxy = 'http://PITC-Zscaler-EMEA-Amsterdam3PR.proxy.corporate.gdn.ge.com:80/'
    https_proxy = 'http://PITC-Zscaler-EMEA-Amsterdam3PR.proxy.corporate.gdn.ge.com:80/'
  }
  parameters {
    string(name: 'branch', defaultValue: 'release-ngc-m3', description: 'git branch')
  }
}