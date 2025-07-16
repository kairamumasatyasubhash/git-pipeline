pipeline {
    agent any // This pipeline can run on any available agent

    stages {
        stage('Build Project') {
            steps {
                // The 'dir' step creates a directory (if it doesn't exist)
                // and changes the current working directory for the steps inside it.
                dir('subhashkairam') {
                    echo "Now inside the 'subhashkairam' directory."

                    // Step 1: Clone the repository
                    // It's best practice to use the built-in 'git' step.
                    echo "Cloning the repository..."
                    git url: 'https://github.com/kairamumasatyasubhash/git-pipeline.git'

                    // Step 2: Build the project inside the cloned repository
                    // We need to change into the 'git-pipeline' directory before running Maven.
                    echo "Changing into the cloned repository directory..."
                    dir('git-pipeline') {
                        echo "Now inside 'git-pipeline'. Running Maven build..."

                        // This assumes your Jenkins agent has Maven configured.
                        // On Windows, you would use bat 'mvn clean install'
                        if (isUnix()) {
                           sh 'mvn clean install'
                        } else {
                           bat 'mvn clean install'
                        }

                        echo "Maven build complete."
                    }
                }
            }
        }
    }
    post {
        always {
            echo "Pipeline finished."
        }
    }
}
