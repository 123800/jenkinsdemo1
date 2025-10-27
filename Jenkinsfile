pipeline {
    agent any

    environment {
        PYTHON = 'C:\\Users\\kiran\\AppData\\Local\\Microsoft\\WindowsApps\\python.exe'
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Setup Python') {
            steps {
                bat "${env.PYTHON} --version"
            }
        }

        stage('Extract') {
            steps {
                bat "${env.PYTHON} extract.py"
            }
        }
    }

    post {
        always {
            echo 'Pipeline completed.'
        }
       success {
            echo 'Pipeline completed.'
        }
        failure {
            echo 'Pipeline failed.'
        }

    }
}

