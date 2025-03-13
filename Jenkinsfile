pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/NishitaE-26/PES1UG22AM109_Jenkins'
            }
        }
        stage('Build') {
            steps {
                sh 'g++ -o output hello.cpp'
            }
        }
        stage('Test') {
            steps {
                sh './output'  // Adjust this if it's a test command        
        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully.'
        }
        failure {
            echo 'Pipeline failed.'
        }
    }
}
