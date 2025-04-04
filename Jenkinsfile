// Declarative Pipeline
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // This will automatically checkout your SCM
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building..'
                // Add your build commands here
            }
        }

        stage('Test') {
            steps {
                echo 'Testing..'
                // Add your test commands here
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying....'
                // Add your deployment commands here
            }
        }
    }

    post {
        always {
            echo 'Pipeline completed'
        }
        success {
            echo 'Pipeline succeeded!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
