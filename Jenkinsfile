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

        stage('Docker Login') {
            steps {
                withCredentials([usernamePassword(credentialsId: 'dockerhub-cred', usernameVariable: 'USER', passwordVariable: 'PASS')]) {
                    sh 'echo $PASS | docker login -u $USER --password-stdin'
                }
            }
        }

        stage('Push Docker Image') {
            steps {
                sh 'docker push niteshmishra12/devops-static-site'
            }
        }

    }
}
