pipeline {
   agent any
  stages {
      stage('git checkout') {
        steps {
            git 'https://github.com/leostanley1210/Chat_Room.git'  
        }
      }
      stage('docker build') {
        steps {
            script {
              sh 'docker build -t chat-room .' 
            }
      }
    }
   stage('docker container') {
         steps {
            script {
               sh 'docker run -itd --name chat-room -p 8082:8080 chat-room'
              }
          }
    }    
  }
}       
   
