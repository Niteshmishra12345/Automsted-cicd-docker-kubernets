pipeline {
    agent any

    stages {

        stage('Clone Code') {
            steps {
                git 'https://github.com/Niteshmishra12345/automated-cicd-docker-kubernets.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t niteshmishra12/devops-static-site ./website'
            }
        }

        stage('Push Docker Image') {
            steps {
                sh 'docker push niteshmishra12/devops-static-site'
            }
        }

    }
}
