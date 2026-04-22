pipeline {
  agent none
  stages {
    stage("build and test the project") {
      agent {
          docker "python:2"
      }
      stages {
        stage('No contenedor') {
          steps {
              sh 'python --version'
          }
        }
      }
    }
    stage("deploy in production") {
      agent any
      stages {
        stage('Na máquina') {
          steps {
              sh 'python3 --version'
          }
        }
      }
    }
  }
}
