pipeline {
  agent any
  stages {
    stage('first') {
      steps {
        sh 'docker run -d -p 9090:8080 --name=tom1 tomcat'
      }
    }

  }
  environment {
    http_proxy = 'http://PITC-Zscaler-EMEA-Amsterdam3PR.proxy.corporate.gdn.ge.com:80/'
    https_proxy = 'http://PITC-Zscaler-EMEA-Amsterdam3PR.proxy.corporate.gdn.ge.com:80/'
  }
}