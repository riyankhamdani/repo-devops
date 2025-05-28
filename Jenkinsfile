pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/riyankhamdani/repo-devops.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'echo "Build image here"'
            }
        }

        stage('Run Grafana Container') {
            steps {
                sh 'echo "Run container here"'
            }
        }

        stage('Katalon Test (Manual Trigger)') {
            steps {
                input "Run Katalon test?"
                sh 'echo "Run Katalon test here"'
            }
        }
    }
}
