pipeline {
  agent any
  stages {


    stage('git clone!!!! ') {
      steps {
        sh '''
        sudo rm -rf /root/var/lib/jenkins/workspace/freesias/freesia
        sudo git clone https://github.com/coldpaper1/fressia.git
        cd freesia


        sudo chmod 777 build-update.yaml
        '''
      }
    }
    stage('docker build & push & rolling-update ') {
      steps {
        sh '''

        sudo ansible-playbook build-update.yaml

        '''
      }
    }

  }
}
