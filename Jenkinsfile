pipeline {
  agent any
  stages {
    stage('123') {
      steps {
        echo '1'
      }
    }

    stage('a') {
      steps {
        sh '''
             export ISO_PATH=/home/shr_mibuilder/Desktop/html
             cd $ISO_PATH
              d=$(ls -td -- * | head -n 1)
              export ISO_PATH=$ISO_PATH$d
              echo $ISO_PATH
              echo $d
        
        '''
      }
    }

  }
}