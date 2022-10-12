pipeline {
  agent any
  stages {
    stage('Clone') {
      steps {
        catchError(buildResult: 'success', stageResult: 'success') {
          sh '''
            export version=0.0.2
            echo $version'''
        }

      }
    }

  }
  parameters {
    string(name: 'scut_branch', defaultValue: 'master', description: 'branch for SCUT git sources')
    string(name: 'version', defaultValue: '0.0.1', description: 'version')
  }
}