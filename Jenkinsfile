pipeline {
    agent {
        docker { image 'python:2' }
    }
    stages {
        stage('Test') {
            steps {
                sh 'python --version'
            }
        }
    }
}