pipeline {
  agent any
  stages {
    stage('Clone') {
      steps {
        sh '''export current_epoch=$(date +%s.%N)
export target_epoch=$(date -d "18:08:08.12345" +%s.%N)

export sleep_seconds=$(echo "$target_epoch - $current_epoch"|bc)

sleep $sleep_seconds'''
      }
    }

  }
  environment {
    TEMP_DIR = '/home/shr_mibuilder/Desktop/'
  }
}