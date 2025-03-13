pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/NishitaE-26/PES1UG22AM109_Jenkins'
            }
        }

        stage('Build') {
            steps {
                sh 'ls -R'  // Debugging step to see the file structure
                sh 'g++ -o output hello.cpp'
            }
        }

        stage('Test') {
            steps {
                sh './output'  // Run the compiled program (if it has a main function)
            }
        }

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
