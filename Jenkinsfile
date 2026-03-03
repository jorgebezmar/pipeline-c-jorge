pipeline {
    agent any

    stages {

        stage('Clonación') {
            steps {
                echo 'Clonando el repositorio remoto...'
                checkout scm
            }
        }

        stage('Compilación') {
            steps {
                echo 'Compilando el proyecto...'
                sh 'gcc -c app.c'
            }
        }

        stage('Tests') {
            steps {
                echo 'Realizando Pruebas Unitarias...'
                sh 'gcc -o test_app app.c test_app.c'
                sh './test_app'
            }
        }

        stage('Despliegue') {
            steps {
                echo 'En un futuro desplegaremos la aplicación!!'
            }
        }
    }
}
