pipeline {
    agent any

    stages {
        stage('dev') {
            steps {
                echo 'executing sum of 2 & 3'
                sh 'chmod +x scripts/testing.sh'
                sh './testing.sh' 
            }
        }        
    }
}