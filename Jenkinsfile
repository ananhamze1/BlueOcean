pipeline {
  agent any
  stages {
    stage('Clone') {
      steps {
        sh '''
         echo $?
           if [ $? -nq 0 ] 
           then
              exit 1
            fi

          '''
      }
    }

  }
  parameters {
    string(name: 'scut_branch', defaultValue: 'master', description: 'branch for SCUT git sources')
    string(name: 'version', defaultValue: '', description: 'version')
  }
}