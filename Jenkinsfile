pipeline {
  agent any
  stages {
    stage('Clone') {
      steps {
        sh '''export current_epoch=$(date -d "21:00:00" +%s)
export target_epoch=$(date -d "18:00:00" +%s)

export sleep_seconds=$(echo "$target_epoch - $current_epoch"|bc)

echo $sleep_seconds

export current_epoch=$(date -d "21:00:00" +%s)
export target_epoch=$(date -d "00:00:00" +%s)

export sleep_seconds=$(echo "$target_epoch - $current_epoch"|bc)

echo $sleep_seconds

export current_epoch=$(date -d "21:00:00" +%s)
export target_epoch=$(date -d "18:00:00" +%s)

export sleep_seconds=$(echo "$target_epoch - $current_epoch"|bc)

echo $sleep_seconds'''
      }
    }

  }
  environment {
    TEMP_DIR = '/home/shr_mibuilder/Desktop/'
  }
}