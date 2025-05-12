pipeline {
   agent any
  stages {
      stage('git checkout') {
        steps {
            git 'https://github.com/leostanley1210/Chat_Room.git'  
        }
      }
      stage('mvn build') {
        steps {
            script {
              sh 'mvn clean install' 
            }
      }
    }
  }  
}
