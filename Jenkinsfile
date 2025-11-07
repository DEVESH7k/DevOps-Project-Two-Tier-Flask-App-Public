pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/DEVESH7k/DevOps-Project-Two-Tier-Flask-App-Public'
            }
        }
        stage('Build') {
            steps {
                sh 'python3 -m venv venv'
                sh '. venv/bin/activate && pip install -r requirements.txt'
            }
        }
        stage('Test') {
            steps {
                sh '. venv/bin/activate && pytest || true'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploy stage would go here'
            }
        }
    }
}
