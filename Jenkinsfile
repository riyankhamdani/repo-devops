pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/riyankhamdani/repo-devops.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t mygrafana:latest .'
            }
        }

        stage('Run Grafana Container') {
            steps {
                sh 'docker rm -f grafana || true'
                sh 'docker run -d --name grafana -p 3000:3000 mygrafana:latest'
            }
        }

        stage('Katalon Test (Manual Trigger)') {
            steps {
                echo 'Testing dilakukan via Katalon Studio di lokal'
            }
        }
    }
}
