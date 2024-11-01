pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps{
            checkout scm
            }
        }
        stage('Build') {
    steps {
        sh '/opt/homebrew/bin/npm install'
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
