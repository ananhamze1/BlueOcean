pipeline {
  agent any
  stages {
    stage('Clone') {
      steps {
        sh 'exit 0'
      }
    }

  }
  parameters {
    string(name: 'scut_branch', defaultValue: 'master', description: 'branch for SCUT git sources')
    string(name: 'version', defaultValue: '', description: 'version')
  }
}