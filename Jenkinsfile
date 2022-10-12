pipeline {
  agent any
  stages {
    stage('Clone') {
      steps {
        catchError(buildResult: 'success', stageResult: 'success') {
          sh '''
            if [$version== ""]; then
                export version=0.0.2
            fi

            echo $version

            regex="([0-9]+).([0-9]+).([0-9]+)"
            if [[ $version =~ $regex ]]; then
              major="${BASH_REMATCH[1]}"
              minor="${BASH_REMATCH[2]}"
              build="${BASH_REMATCH[3]}"
            fi
            minor=$(echo $minor + 1 | bc)
            build=$(echo $build + 1 | bc)
            major=$(echo $major + 1 | bc)
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