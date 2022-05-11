pipeline {
  agent any
  stages {
    stage('123') {
      steps {
        echo '3'
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