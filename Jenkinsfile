pipeline {

  agent any 

  stages {

    stage ('Molecule test') {
      steps {
        sh '''
          molecule test
        '''
      }
    }

    stage ('Deploy the shit to another machine') {
      steps {
        sh '''
          ssh 192.168.0.36 git clone https://github.com/pscsys/ansible-motd /tmp/ansible-motd
        '''
      }
    }

  }
}