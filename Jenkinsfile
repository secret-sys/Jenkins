pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                git 'https://github.com/secret-sys/Jenkins.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                bat 'npm install'  // instead of sh 'npm install'
            }
        }

        stage('Run Tests') {
            steps {
                bat 'npm test'  // instead of sh 'npm test'
            }
        }

        stage('Deploy') {
            steps {
                bat 'npm run deploy'  // if applicable
            }
        }
    }
}
