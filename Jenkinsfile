pipeline {
    agent any

    stages {

        stage('Clone Repository') {
            steps {
                echo 'Cloning repository:'
                git branch: 'main', url: 'https://github.com/youssefabdulmoneim/CloudTask4.git'
            }
        }

        stage('Build') {
            steps {
                echo 'No compilation needed for Python. Python version is:'
                sh 'python3 --version'
            }
        }

        stage('Run Unit Tests') {
            steps {
                echo 'Running unit tests:'
                sh 'python3 -m pytest calculator_test.py -v'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully! All tests passed.'
        }
        failure {
            echo 'Pipeline failed. Check the logs above.'
        }
    }
}