pipeline {
  agent any
  stages{
    stage('ssh-local machine  accesss') {
      steps {
        sshpass -p usernotfound ssh anilkumar@192.168.196.188 'sudo docker kill $(sudo docker ps -q)'
      }
    }
  }
}
