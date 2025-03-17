pipeline {
    agent any
    tools {
        maven 'maven'
        jdk 'java-17'
    }

    stages {
        stage('GIT SCM') {
            steps {
                git 'https://github.com/leostanley1210/Chat_Room.git'
            }
        }
        stage (compile) {
            steps {
                bat 'mvn compile'
            }
        }
           
        }
        stage('build'){
            steps { bat 'mvn package'
           }
         }
    }
}