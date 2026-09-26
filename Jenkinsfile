pipeline {
    agent any

    environment {
        APP_NAME = 'test'
    }

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out code'
            }
        }

        stage('Test') {
            steps {
                sh 'echo running tests'
            }
        }
    }

    post {
        success {
            echo 'All stages passed'
        }

        failure {
            echo 'Something failed'
        }
    }
}
