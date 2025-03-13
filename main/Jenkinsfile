pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -o output YOUR_SRN-1/main.cpp'
            }
        }

        stage('Test') {
            steps {
                sh './output'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment stage (not actually deploying anything in this example)'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
