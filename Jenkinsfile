pipeline {
    agent any

    environment {
        PIP = 'D:\\Python\\Scripts\\pip.exe'
        PYTHON = 'D:\\Python\\python.exe'
    }

    stages {
        stage('Clone Repo') {
            steps {
                git branch: 'main', url: 'https://github.com/secret-sys/Jenkins.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                bat "${PIP} install --upgrade pip"
                bat "${PIP} install -r requirements.txt"
            }
        }

        stage('Run Tests') {
            steps {
                // Replace with your actual test framework
                bat "${PYTHON} -m unittest discover tests"
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying Application...'
                // Add actual deployment steps here
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed!'
        }
        success {
            echo 'Pipeline succeeded!'
        }
    }
}
