
pipeline {
    agent any

    environment {
        PYTHON = 'C:\\Program Files\\Python313\\python.exe'
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
                bat "${env.C:\\Program Files\\Python313\\python.exe
} extract.py"
            }
        }
    }

    post {
        always {
            echo 'Pipeline completed.'
        }
    }
}
