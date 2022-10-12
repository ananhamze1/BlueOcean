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
            major="${version[1]}"
            minor="${version[2]}"
            build="${version[3]}"
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
    string(name: 'version', defaultValue: '', description: 'version')
  }
}