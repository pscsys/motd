pipeline {

  agent any 

  stages {

    stage ('Molecule test') {
      steps {
        sh '''
          export PATH="$PATH:/var/lib/jenkins/.local/bin/molecule"
          molecule test
        '''
      }
    }

    stage ('Deploy the shit to another machine') {
      steps {
        sh '''
          ssh 192.168.0.39 git clone https://github.com/pscsys/ansible-motd /tmp/ansible-motd
        '''
      }
    }

  }
}
