pipeline {
    agent any

    tools {
        nodejs 'NodeJS 24 LTS'
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/sasankasandeepa152-ship-it/simple-node-app.git'
            }
        }

        stage('Install') {
            steps {
                bat 'node --version'
                bat 'npm --version'
                bat 'npm install'
            }
        }

        stage('Test') {
            steps {
                bat 'npm test'
            }
        }

        stage('Run') {
            steps {
                bat 'npm start'
            }
        }
    }
}
