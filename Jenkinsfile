pipeline {
    agent any

    stages {
        // Remove the 'Clone Repo' stage entirely
        // Jenkins will handle the checkout based on the job configuration
        stage('Install Dependencies') {
    steps {
        bat '"C:\\Path\\To\\pip.exe" install -r requirements.txt'
    }
}

        stage('Run Tests') {
            steps {
                sh 'pytest'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploy step (optional)'
                // For actual deployment: SCP, Docker, etc.
            }
        }
    }
}