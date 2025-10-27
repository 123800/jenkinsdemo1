pipeline {
    agent any

    stages {
        stage('Checkout code') {
            steps {
                checkout scm
            }
        }

        stage('Install dependencies') {
            steps {
                bat 'python -m pip install --upgrade pip'
                bat 'pip install -r requirements.txt'
            }
        }

        stage('Run Python Script') {
            steps {
                bat 'python extract.py'
            }
        }
    }

    post {
        always {
            echo 'Pipeline completed.'
        }
    }
}

