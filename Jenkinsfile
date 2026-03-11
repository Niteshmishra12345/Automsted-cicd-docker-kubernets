pipeline {
    agent any

    stages {

        stage('Clone Repository') {
            steps {
                git 'https://github.com/Niteshmishra12345/automated-cicd-docker-kubernets.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t devops-static-site ./website'
            }
        }

        stage('Run Docker Container') {
            steps {
                sh 'docker run -d -p 8080:80 devops-static-site'
            }
        }

    }
}
