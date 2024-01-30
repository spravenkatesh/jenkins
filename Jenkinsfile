pipeline {
    agent any

    stages {
        stage('dev-bash') {
            steps {
                echo 'executing sum of 2 & 3'
                sh 'chmod +x scripts/testing.sh'
                sh './scripts/testing.sh' 
            }
        }
        stage('dev-python') {
            steps {
                echo 'executing python script'
                sh 'python /scripts/testing.py'
            }
        }        
    }
}