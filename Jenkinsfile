pipeline {
    agent any 
    stages {
        stage ('Git Clone') {
            steps {
                sh '''
                dir ('subhashkairam')
                git clone https://github.com/kairamumasatyasubhash/git-pipeline.git
                mvn clean install
                '''
            }
        }
    }
}
