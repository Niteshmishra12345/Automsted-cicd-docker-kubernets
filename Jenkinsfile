pipeline {
    agent any

    stages {

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t static-site ./website'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 8082:80 static-site'
            }
        }

    }
}
