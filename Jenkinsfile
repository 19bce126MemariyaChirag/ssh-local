pipeline {
  agent any
  stages{
    stage('ssh-local machine  accesss') {
      steps {
        sshpass -p meet ssh meetshah@172.16.1.123 'sudo docker kill $(sudo docker ps -q)'
      }
    }
  }
}
