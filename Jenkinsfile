pipeline {
    agent any
    environment {
        CI = 'true'
    }
    stages {
        stage('Test') {
            steps {
                sh './scripts/test.sh'
            }
        }
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Deliver') {
            steps {
                sh './scripts/deploy.sh'
                input message: 'Finished using the web site? (Click "Proceed" to continue)'
                sh './scripts/kill.sh'
            }
        }
    }
}