pipeline {
  agent any
  stages {
    stage('Clone') {
      steps {
        sh 'date -d "$Tandem_Unified_SLES:00:00" +%s'
        sh '''if [ $NGC -gt 21 ]
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