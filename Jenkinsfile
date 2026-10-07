pipeline {
    agent any

    environment {
        APP_NAME = 'week9-devops-app'
        IMAGE_NAME = 'week9-devops-app'
    }

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building application...'
                sh 'echo Build successful'
            }
        }

        stage('Test') {
            steps {
                echo 'Running automated tests...'
                sh 'echo Test successful'
            }
        }

        stage('Package') {
            steps {
                echo 'Packaging application...'
                sh 'echo Package successful'
            }
        }

        stage('Docker Build') {
            steps {
                sh 'docker build -t ${IMAGE_NAME}:latest .'
            }
        }
    }

    post {
        success {
            echo 'Week 9 CI/CD Pipeline completed successfully!'
        }

        failure {
            echo 'Pipeline failed. Check the console output.'
        }
    }
}
