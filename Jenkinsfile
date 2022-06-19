pipeline {
  agent any
  stages {


    stage('git clone!!!! ') {
      steps {
        sh '''
        sudo rm -rf /var/lib/jenkins/workspace/freesia
        sudo git clone https://github.com/coldpaper1/fressia.git
        

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
