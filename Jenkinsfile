pipeline {
    agent any
    stages {
        stage ('Git Checkout') {
            steps{
                checkout scm
                echo "Code checked sucessfully"
            }
        }
        stage ('Build') {
            steps {
                echo "Building the Project ...."
                bat 'dir'
                sh 'ls -l'
            }
        }
        stage ('Test') {
            steps {
                echo "Running the test ...."
            }
        }
    }
}
