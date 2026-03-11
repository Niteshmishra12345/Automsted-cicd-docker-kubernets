pipeline {
    agent any
    
    environment {
        // Add this
        GIT_CREDS = credentials('github-token')
    }
    
    stages {
        stage('Checkout Code') {
            steps {
                // Fix 1: First checkout - with credentials
                git branch: 'main',
                    url: 'https://github.com/Niteshmishra12345/Automsted-cicd-docker-kubernets.git',
                    credentialsId: 'github-toke'
            }
        }
        
        stage('Clone Repository') {
            steps {
                // Fix 2: Second checkout - with credentials
                git branch: 'main',
                    url: 'https://github.com/Niteshmishra12345/automated-cicd-docker-kubernets.git',
                    credentialsId: 'github-token'   
            }
        }
        
        // Rest of your pipeline...
    }
}
