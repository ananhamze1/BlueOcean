pipeline {
  agent any
  stages {
    stage('Clone') {
      steps {
        sh '''
export current_epoch=$(date -d "21:00:00" +%s)
export target_epoch=$(date -d "18:00:00" +%s)

export sleep_seconds=$(echo "$target_epoch - $current_epoch"|bc)

echo $sleep_seconds

export current_epoch=$(date -d "21:00:00" +%s)
export target_epoch=$(date -d "23:59:59" +%s)

export sleep_seconds=$(echo "$target_epoch - $current_epoch"|bc)

echo $sleep_seconds

export current_epoch=$(date -d "21:00:00" +%s)
export target_epoch=$(date -d "18:00:00" +%s)

export sleep_seconds=$(echo "$target_epoch - $current_epoch"|bc)

echo $sleep_seconds'''
        sh '''if [ $Tandem_Unified_SLES -gt 21 ]
then
echo "11"
else
echo "22"
fi'''
      }
    }

  }
  environment {
    TEMP_DIR = '/home/shr_mibuilder/Desktop/'
  }
  parameters {
    string(name: 'NGC', defaultValue: '2', description: 'NGC trigger time')
    string(name: 'SmartConsole', defaultValue: '21', description: 'SmartConsole trigger time')
    string(name: 'SmartConsole_SLES', defaultValue: '23', description: 'SmartConsole SLES trigger time')
    string(name: 'Stargate', defaultValue: '1', description: 'Stargate trigger time')
    string(name: 'Stargate_SLES', defaultValue: '1', description: 'Stargate SLES trigger time')
    string(name: 'Tandem_Unified', defaultValue: '21', description: 'Tandem Unified trigger time')
    string(name: 'Tandem_Unified_SLES', defaultValue: '23', description: 'Tandem Unified SLES trigger time')
  }
}