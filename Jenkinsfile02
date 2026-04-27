pipeline {
    agent {
        docker { image 'python:3' }
    }
    stages {
        stage('Test') {
            steps {
                sh 'python -m unittest test_utils.py'
            }
        }
    }
}
