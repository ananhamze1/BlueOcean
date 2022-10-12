pipeline {
  agent any
  stages {
    stage('Clone') {
      steps {
        catchError(buildResult: 'success', stageResult: 'success') {
          sh '''

            echo $version
            regex="([0-9]+).([0-9]+).([0-9]+)"
            if [[ $version =~ $regex ]]; then
              echo $version
            else
              version=$(cat /home/shr_mibuilder/Desktop/c.txt)
            fi
            major="${BASH_REMATCH[1]}"
            minor="${BASH_REMATCH[2]}"
            build="${BASH_REMATCH[3]}"
            build=$(echo $build + 1 | bc)
            export next_version=${major}.${minor}.${build}
            
            echo $next_version > /home/shr_mibuilder/Desktop/c.txt
            echo $next_version
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