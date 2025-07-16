pipeline {
    agent any // This pipeline can run on any available agent

    stages {
        stage('Create Directory and Clone') {
            steps {
                echo "Preparing to clone the repository into a new directory..."
                git(
                    url: 'https://github.com/kairamumasatyasubhash/git-pipeline.git', // Added comma here
                    branch: 'main',
                    dir: 'pipeline-git' // This directory will be created
                )

                echo "Repository cloned successfully into the 'pipeline-git' directory." // Corrected directory name
            }
        }

        stage('Verify Cloned Directory') {
            steps {
                dir('pipeline-git') {
                    echo "Verifying contents of the cloned directory..."
                    script {
                        if (isUnix()) {
                            sh 'ls -la'
                        } else {
                            bat 'dir'
                        }
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
