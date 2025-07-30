pipeline {
    agent any

    stages {
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