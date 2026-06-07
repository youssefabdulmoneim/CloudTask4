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
                bat '"C:\\msys64\\mingw64\\bin\\python.exe" --version'
            }
        }

        stage('Run Unit Tests') {
            steps {
                echo 'Running unit tests:'
                bat '"C:\\msys64\\mingw64\\bin\\python.exe" -m unittest calculator_test.py -v'
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
