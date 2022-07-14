pipeline {
  agent any
  stages {
    stage('Clone_SmartConsole ') {
      parallel {
        stage('Clone_SmartConsole ') {
          post {
            success {
              sh 'echo "$STAGE_NAME: PASS --" >> /home/shr_mibuilder/Desktop/html/stages.txt'
            }

            failure {
              sh 'echo "$STAGE_NAME: FAIL DevOps_Team_To_Investigate" >> /home/shr_mibuilder/Desktop/html/stages.txt'
            }

          }
          steps {
            script {
              CLONE_SMARTCONSOL = '<b><font color=red>FAIL</font></b>'
              CLONE_SMARTCONSOL_OWNER = '<b><font color=black>DevOps Team To Investigate</font></b>'
              sh'''echo "$STAGE_NAME: FAIL DevOps_Team_To_Investigate" >> /home/shr_mibuilder/Desktop/html/stages.txt'''
            }

            script {
              CLONE_SMARTCONSOL = '<b><font color=green>PASS</font></b>'
              CLONE_SMARTCONSOL_OWNER = '<b><font color=black>--</font></b>'
            }

          }
        }

        stage('Clone_Anonymizer') {
          post {
            success {
              sh 'echo "$STAGE_NAME: PASS --" >> /home/shr_mibuilder/Desktop/html/stages.txt'
            }

            failure {
              sh 'echo "$STAGE_NAME: FAIL DevOps_Team_To_Investigate" >> /home/shr_mibuilder/Desktop/html/stages.txt'
            }

          }
          steps {
            script {
              CLONE_ANONYMIZER = '<b><font color=red>FAIL</font></b>'
              CLONE_ANONYMIZER_OWNER = '<b><font color=black>DevOps Team To Investigate</font></b>'
            }

            script {
              CLONE_ANONYMIZER = '<b><font color=green>PASS</font></b>'
              CLONE_ANONYMIZER_OWNER = '<b><font color=black>--</font></b>'
            }

          }
        }

      }
    }

    stage('Update_Version') {
      post {
        success {
          sh 'echo "$STAGE_NAME: PASS --" >> /home/shr_mibuilder/Desktop/html/stages.txt'
        }

        failure {
          sh 'echo "$STAGE_NAME: FAIL DevOps_Team_To_Investigate" >> /home/shr_mibuilder/Desktop/html/stages.txt'
        }

      }
      steps {
        script {
          UPDATE_VERSION = '<b><font color=red>FAIL</font></b>'
          UPDATE_VERSION_OWNER = '<b><font color=black>DevOps Team To Investigate</font></b>'
        }

        script {
          UPDATE_VERSION = '<b><font color=green>PASS</font></b>'
          UPDATE_VERSION_OWNER = '<b><font color=black>--</font></b>'
        }

      }
    }

    stage('Build_CPP') {
      post {
        success {
          sh 'echo "$STAGE_NAME: PASS --" >> /home/shr_mibuilder/Desktop/html/stages.txt'
        }

        failure {
          sh 'echo "$STAGE_NAME: FAIL DevOps_Team_To_Investigate" >> /home/shr_mibuilder/Desktop/html/stages.txt'
        }

      }
      steps {
        script {
          BUILD_CPP = '<b><font color=red>FAIL</font></b>'
          Build_CPP_OWNER = '<b><font color=black>SmartConsole Team To Investigate</font></b>'
        }

        script {
          BUILD_CPP = '<b><font color=green>PASS</font></b>'
          BUILD_CPP_OWNER = '<b><font color=black>--</font></b>'
        }

      }
    }

    stage('ReconBoxWebParent') {
      post {
        success {
          sh 'echo "$STAGE_NAME: PASS --" >> /home/shr_mibuilder/Desktop/html/stages.txt'
        }

        failure {
          sh 'echo "$STAGE_NAME: FAIL SmartConsole_Team_To_Investigate" >> /home/shr_mibuilder/Desktop/html/stages.txt'
        }

      }
      steps {
        script {
          RECON_BOX = '<b><font color=red>FAIL</font></b>'
          RECON_BOX_OWNER = '<b><font color=black>SmartConsole Team To Investigate</font></b>'
        }

        script {
          RECON_BOX = '<b><font color=green>PASS</font></b>'
          RECON_BOX_OWNER = '<b><font color=black>--</font></b>'
        }

      }
    }

    stage('Build BE & FE') {
      parallel {
        stage('Build_Java') {
          environment {
            RBOX_ROOT = '/home/ctuser/falcon'
            HOME = '/home/ctuser'
          }
          post {
            success {
              sh 'echo "$STAGE_NAME: PASS --" >> /home/shr_mibuilder/Desktop/html/stages.txt'
            }

            failure {
              sh 'echo "$STAGE_NAME: FAIL SmartConsole_Team_To_Investigate" >> /home/shr_mibuilder/Desktop/html/stages.txt'
            }

          }
          steps {
            script {
              BUILD_JAVA = '<b><font color=red>FAIL</font></b>'
              BUILD_JAVA_OWNER = '<b><font color=black>SmartConsole Team To Investigate</font></b>'
            }

            script {
              BUILD_JAVA = '<b><font color=green>PASS</font></b>'
              BUILD_JAVA_OWNER = '<b><font color=black>--</font></b>'
            }

          }
        }

        stage('Build_JS') {
          environment {
            RBOX_ROOT = '/home/ctuser/falcon'
          }
          post {
            success {
              sh 'echo "$STAGE_NAME: PASS --" >> /home/shr_mibuilder/Desktop/html/stages.txt'
            }

            failure {
              sh 'echo "$STAGE_NAME: FAIL SmartConsole_Team_To_Investigate" >> /home/shr_mibuilder/Desktop/html/stages.txt'
            }

          }
          steps {
            script {
              BUILD_JS = '<b><font color=red>FAIL</font></b>'
              BUILD_JS_OWNER = '<b><font color=black>SmartConsole Team To Investigate</font></b>'
            }

            script {
              BUILD_JS = '<b><font color=green>PASS</font></b>'
              BUILD_JS_OWNER = '<b><font color=black>--</font></b>'
            }

          }
        }

        stage('Anonymizer_Build') {
          post {
            success {
              sh 'echo "$STAGE_NAME: PASS --" >> /home/shr_mibuilder/Desktop/html/stages.txt'
            }

            failure {
              sh 'echo "$STAGE_NAME: FAIL SmartConsole_Team_To_Investigate" >> /home/shr_mibuilder/Desktop/html/stages.txt'
            }

          }
          steps {
            script {
              ANONYMIZER_BUILD = '<b><font color=red>FAIL</font></b>'
              ANONYMIZER_BUILD_OWNER = '<b><font color=black>SmartConsole Team To Investigate</font></b>'
            }

            script {
              ANONYMIZER_BUILD = '<b><font color=green>PASS</font></b>'
              ANONYMIZER_BUILD_OWNER = '<b><font color=black>--</font></b>'
            }

          }
        }

      }
    }

    stage('Scut + Lister') {
      parallel {
        stage('Run_Scut') {
          post {
            success {
              sh 'echo "$STAGE_NAME: PASS --" >> /home/shr_mibuilder/Desktop/html/stages.txt'
            }

            failure {
              sh 'echo "$STAGE_NAME: FAIL SmartConsole_Team_To_Investigate" >> /home/shr_mibuilder/Desktop/html/stages.txt'
            }

          }
          steps {
            script {
              RUN_SCUT = '<b><font color=red>FAIL</font></b>'
              RUN_SCUT_OWNER = '<b><font color=black>SmartConsole Team To Investigate</font></b>'
            }

          }
        }

        stage('Lister') {
          post {
            success {
              sh 'echo "$STAGE_NAME: PASS --" >> /home/shr_mibuilder/Desktop/html/stages.txt'
            }

            failure {
              sh 'echo "$STAGE_NAME: FAIL SmartConsole_Team_To_Investigate" >> /home/shr_mibuilder/Desktop/html/stages.txt'
            }

          }
          steps {
            script {
              LISTER="<b><font color=red>FAIL</font></b>"
              LISTER_OWNER = '<b><font color=black>SmartConsole Team To Investigate</font></b>'
            }

          }
        }

      }
    }

    stage('Create_Docker_ISO') {
      environment {
        RBOX_ROOT = '/home/ctuser/falcon'
      }
      post {
        success {
          sh 'echo "$STAGE_NAME: PASS --" >> /home/shr_mibuilder/Desktop/html/stages.txt'
        }

        failure {
          sh 'echo "$STAGE_NAME: FAIL SmartConsole_Team_To_Investigate" >> /home/shr_mibuilder/Desktop/html/stages.txt'
        }

      }
      steps {
        script {
          DOCKER_ISO = '<b><font color=red>FAIL</font></b>'
          DOCKER_ISO_OWNER = '<b><font color=black>DevOps Team To Investigate</font></b>'
        }

        script {
          DOCKER_ISO = '<b><font color=green>PASS</font></b>'
          DOCKER_ISO_OWNER = '<b><font color=black>--</font></b>'
        }

      }
    }

    stage('Deployment') {
      parallel {
        stage('Deploy_Artifacts ') {
          post {
            success {
              sh 'echo "$STAGE_NAME: PASS --" >> /home/shr_mibuilder/Desktop/html/stages.txt'
            }

            failure {
              sh 'echo "$STAGE_NAME: FAIL SmartConsole_Team_To_Investigate" >> /home/shr_mibuilder/Desktop/html/stages.txt'
            }

          }
          steps {
            script {
              DEPLOY_ARTIFACTS = '<b><font color=red>FAIL</font></b>'
              DEPLOY_ARTIFACTS_OWNER = '<b><font color=black>DevOps Team To Investigate</font></b>'
            }

            script {
              DEPLOY_ARTIFACTS = '<b><font color=green>PASS</font></b>'
              DEPLOY_ARTIFACTS_OWNER = '<b><font color=black>--</font></b>'
            }

          }
        }

      }
    }

  }
  environment {
    CLONE_SMARTCONSOL = '<b><font color=red>--</font></b>'
    CLONE_ANONYMIZER = '<b><font color=red>--</font></b>'
    UPDATE_VERSION = '<b><font color=red>--</font></b>'
    BUILD_CPP = '<b><font color=red>--</font></b>'
    RECON_BOX = '<b><font color=red>--</font></b>'
    BUILD_JAVA = '<b><font color=red>--</font></b>'
    BUILD_JS = '<b><font color=red>--</font></b>'
    ANONYMIZER_BUILD = '<b><font color=red>--</font></b>'
    RUN_SCUT = '<b><font color=red>--</font></b>'
    LISTER = '<b><font color=red>--</font></b>'
    DOCKER_ISO = '<b><font color=red>--</font></b>'
    DEPLOY_ARTIFACTS = '<b><font color=red>--</font></b>'
    EMAIL_BODY = ' '
    CLONE_SMARTCONSOL_OWNER = '<b><font color=black>--</font></b>'
    CLONE_ANONYMIZER_OWNER = '<b><font color=black>--</font></b>'
    UPDATE_VERSION_OWNER = '<b><font color=black>--</font></b>'
    BUILD_CPP_OWNER = '<b><font color=black>--</font></b>'
    RECON_BOX_OWNER = '<b><font color=black>--</font></b>'
    BUILD_JAVA_OWNER = '<b><font color=black>--</font></b>'
    BUILD_JS_OWNER = '<b><font color=black>--</font></b>'
    ANONYMIZER_BUILD_OWNER = '<b><font color=black>--</font></b>'
    RUN_SCUT_OWNER = '<b><font color=black>--</font></b>'
    LISTER_OWNER = '<b><font color=black>--</font></b>'
    DOCKER_ISO_OWNER = '<b><font color=black>--</font></b>'
    DEPLOY_ARTIFACTS_OWNER = '<b><font color=black>--</font></b>'
  }
  post {
    always {
      script {
        if("${currentBuild.result}" == 'ABORTED'){
          RESULT = "<b><font color=orange>UNSTABLE </font></b>"
        }
        if("${currentBuild.result}" == 'SUCCESS'){
          RESULT = "<b><font color=green>SUCCESS</font></b>"
        }
        if("${currentBuild.result}" == 'FAILURE'){
          RESULT = "<b><font color=red>FAILURE</font></b>"
        }
        if("${currentBuild.result}" == 'ABORTED'){
          RESULT = "<b><font color=gray>ABORTED</font></b>"
        }
        EMAIL = 'Rawad.Khalaila@ge.com'
        sh'''
cd /home/shr_mibuilder/Desktop/html
generate.sh < stages.txt > table.txt
tr --delete '\n' < table.txt > text.txt
#set EMAIL_BODY=`cat text.txt`
'''
      }

    }

  }
  options {
    timeout(time: 3, unit: 'HOURS')
  }
  parameters {
    string(name: 'sc_branch', defaultValue: 'develop_sles', description: 'branch for Smartconsole git sources')
    string(name: 'lister_branch', defaultValue: 'develop_sles', description: 'branch for Lister git sources')
    string(name: 'scut_branch', defaultValue: 'develop_sles', description: 'branch for SCUT git sources')
    string(name: 'NmAnonymizer_branch', defaultValue: 'develop_sles', description: 'branch for NmAnonymizer git sources')
    string(name: 'sc_version', defaultValue: '', description: 'smartconsole version - if the version is empty will take from file')
    booleanParam(name: 'nightly', defaultValue: true, description: 'nightly build')
  }
}