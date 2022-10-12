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
              major="${BASH_REMATCH[1]}"
              minor="${BASH_REMATCH[2]}"
              build="${BASH_REMATCH[3]}"
              build=$(echo $build + 1 | bc)
              export next_version=${major}.${minor}.${build}
            else
              version=$(cat /home/shr_mibuilder/Desktop/c.txt)
              major="${BASH_REMATCH[1]}"
              minor="${BASH_REMATCH[2]}"
              build="${BASH_REMATCH[3]}"
              build=$(echo $build + 1 | bc)
              export next_version=${major}.${minor}.${build}
            fi
            
            echo $next_version > /home/shr_mibuilder/Desktop/c.txt
            echo $next_version
          '''
        }

      }
    }

  }
  parameters {
    string(name: 'scut_branch', defaultValue: 'master', description: 'branch for SCUT git sources')
    string(name: 'version', defaultValue: '', description: 'version')
  }
}