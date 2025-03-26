pipeline {

    agent { label 'slave' } 

     tools {
        maven 'maven'
    }

    stages {
        stage('Checkout') {
            steps {
                git credentialsId: 'pipe-line', url: 'git@github.com:leostanley1210/Chat_Room.git', branch: 'master'
            }
        }
        stage('compile') {
            steps {
                sh 'mvn compile'
            }
        }
        stage('build') {
            steps {
                sh 'mvn build'
            }
        }
    }
}
