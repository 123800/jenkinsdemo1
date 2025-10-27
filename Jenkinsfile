pipeline {
    agent any

    stages {
        stage('Checkout code') {
            steps {
                // pulls your repo files (including extract.py)
                checkout scm
            }
        }

        stage('Run Python Script') {
            steps {
                // runs extract.py using the Python in PATH
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
