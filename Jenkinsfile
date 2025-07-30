pipeline {
    agent any

    stages {
        stage('Git Clone and Build') {
            steps {
                script {
                    // Create directory if it doesn't exist
                    sh 'mkdir -p subhashkairam'
                    
                    dir('subhashkairam') {
                        // Clone the repository
                        sh 'git clone https://github.com/kairamumasatyasubhash/git-pipeline.git'
                            sh 'mvn clean install'
                        }
                    }
                }
            }
        }
    }
}
