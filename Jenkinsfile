pipeline {
    agent any

    tools {
        jdk 'jdk-17'
    }

    stages {
        stage('Checkout') {
            steps {
                git credentialsId: 'shh-connection', url: 'git@github.com:leostanley1210/Chat_Room.git', branch: 'master'
            }
        }

        stage('compile') {
            steps {
                sh 'mvn compile'
            }
        }

        stage('build') {
            steps {
                sh 'mvn clean package'
            }
        }
    }
}
