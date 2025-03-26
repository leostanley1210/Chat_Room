pipeline {

    agent { label 'slave' } 

    stages {
        stage('Checkout') {
            steps {
                git credentialsId: 'pipe-line', url: 'git@github.com:leostanley1210/Chat_Room.git', branch: 'master'
            }
        }
        stage('compile') {
            steps {
                sh 'make compile'
            }
        }
        stage('build') {
            steps {
                sh 'make build'
            }
        }
    }
}
