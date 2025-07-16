pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout code from Git
                git url: 'https://github.com/kairamumasatyasubhash/git-pipeline.git', branch: 'main'
            }
        }
        stage('Build') {
            steps {
                // Build the application
                sh 'make build'
            }
        }
        stage('Test') {
            steps {
                // Run tests
                sh 'make test'
            }
        }
        stage('Deploy') {
            steps {
                // Deploy the application
                sh 'make deploy'
            }
        }
    }
}
