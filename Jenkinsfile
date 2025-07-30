pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/vishnupriya-ran/quicknote-simple.git'
            }
        }

        stage('Build and run with docker compose') {
            steps {
                sh '''
                docker-compose down || true
                docker-compose up --build -d
                '''
            }
        }
    }
}