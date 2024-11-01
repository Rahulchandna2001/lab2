pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', credentialsId: 'Rahul', url: 'https://github.com/Rahulchandna2001/lab2.git'
            }
        }
        stage('Build') {
    steps {
        sh 'npm install'
    }
}

        stage('Test') {
            steps {
                sh 'echo Running tests...'
                sh 'npm test'
            }
        }
        stage('Notify') {
            steps {
                script {
                    // For email or Slack notification, add relevant commands or integrations here
                    echo 'Build Completed!'
                }
            }
        }
    }
}