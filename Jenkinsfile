pipeline {
    agent any
    stages {
        stage('Test') {
            steps {
                echo 'This is a test'
                bash 'npm test'
            }
        }
        stage('Build') {
            steps {
                echo 'This is a build'
            }
        }
        stage('Deploy') {
            steps {
                echo 'This is a deploy'
            }
        }
    }
}