pipeline {
  agent any
  stages {
    stage('Clone') {
      steps {
        catchError(buildResult: 'success', stageResult: 'success') {
          sh '''

           echo $version
            regex="([0-9]+).([0-9]+).([0-9]+)"
            if [![ $version =~ $regex ]]; then
              
              version=$(cat /home/shr_mibuilder/Desktop/c.txt)
            fi
            

            echo $version
          '''
        }

      }
    }

  }
  parameters {
    string(name: 'scut_branch', defaultValue: 'master', description: 'branch for SCUT git sources')
    string(name: 'version', defaultValue: '0.0.1', description: 'version')
  }
}