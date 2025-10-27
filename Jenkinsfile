pipeline {
    agent any

    environment {
        PYTHON = '"C:\\Program Files\\Python313\\python.exe"'  
    }

    stages {
        stage('Checkout code') {
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
    }
}
