pipeline {
   agent any
    environment {
     SCANNER_HOME = tool 'sonar-scanner'
    }
   stages {
      stage('git checkout') {
        steps {
            git 'https://github.com/leostanley1210/Chat_Room.git'  
        }
      }
      stage('code analysis') {
        steps {
            withSonarQubeEnv('sonar-server') {
                sh ''' $SCANNER_HOME/bin/sonar-scanner -Dsonar.projectName=Chat_Room \
               -Dsonar.java.binaries=. \
               -Dsonar.projectKey=Chat_Room'''
               }
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
