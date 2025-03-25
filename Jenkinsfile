pipeline {
    agent any
    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/vivek3294/Boundless-Mindz.git'
            }
        }
        stage('Build') {
            steps {
                bat 'npm install'  // Use 'bat' for Windows (instead of 'sh')
            }
        }
        stage('Test') {
            steps {
                bat 'npm test'
            }
        }
        stage('Deploy') {
            steps {
                bat 'pm2 restart server.js'  // Change this to your actual deployment command
            }
        }
    }
}
