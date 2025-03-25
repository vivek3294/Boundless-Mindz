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
                sh 'npm install'  // Install dependencies
            }
        }
        stage('Test') {
            steps {
                sh 'npm test'   // Run tests
            }
        }
        stage('Deploy') {
            steps {
                sh 'pm2 restart server.js'  // Restart the app using PM2
            }
        }
    }
}
 
