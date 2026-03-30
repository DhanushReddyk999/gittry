pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    docker.build('my-node-app')
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    // Run tests if any
                    sh 'npm test'
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    // Example: Run the Docker container
                    sh 'docker run -d -p 8080:8080 my-node-app'
                }
            }
        }
    }

    post {
        always {
            // Clean up
            sh 'docker system prune -f'
        }
    }
}