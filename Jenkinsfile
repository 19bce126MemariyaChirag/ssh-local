pipeline {
  agent any
  stages{
    stage('ssh-local machine  accesss') {
      steps {
        withCredentials([usernameColonPassword(credentialsId: 'anil-ssh', variable: 'anilssh')]) {
    }
      }
    }
  }
}
