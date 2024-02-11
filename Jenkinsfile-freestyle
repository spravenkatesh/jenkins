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
                sh 'chmod +x scripts/testing.py'
                sh '$(which python3) scripts/testing.py'
            }
        }        
    }
}