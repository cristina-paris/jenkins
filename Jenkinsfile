pipeline {
    agent any  // Ejecutar en cualquier agente disponible

    environment {
        NODE_HOME = '/usr/local/bin/node'  // Ruta a tu instalación de Node.js
        PATH = "${NODE_HOME}/bin:${env.PATH}"  // Asegurarse de que Node.js esté en el PATH
    }

    stages {
        stage('Clonar Repositorio') {
            steps {
                git 'https://github.com/tu_usuario/tu_repositorio.git'  // Clonar el repositorio desde GitHub
            }
        }

        stage('Instalar Dependencias') {
            steps {
                script {
                    // Asegúrate de que npm esté disponible y ejecuta 'npm install' para instalar dependencias
                    sh 'npm install'
                }
            }
        }

        stage('Pruebas Unitarias') {
            steps {
                script {
                    // Ejecuta las pruebas unitarias con 'npm test'
                    sh 'npm test'
                }
            }
        }

        stage('Construir Proyecto') {
            steps {
                script {
                    // Ejecuta el proceso de construcción (por ejemplo, empaquetar la aplicación)
                    sh 'npm run build'
                }
            }
        }

        stage('Desplegar') {
            steps {
                script {
                    // Aquí puedes agregar el paso de despliegue, como subir la app a un servidor o hacer deploy a un entorno de prueba
                    echo 'Desplegando la aplicación...'
                }
            }
        }
    }

    post {
        success {
            echo 'Pipeline ejecutado exitosamente.'
        }

        failure {
            echo 'La ejecución del pipeline falló.'
        }
    }
}
