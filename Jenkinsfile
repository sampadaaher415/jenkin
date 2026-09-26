pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'echo Building'
            }
        }

        stage('Test') {
            parallel {
                stage('Unit') {
                    steps {
                        sh 'echo Unit tests'
                    }
                }

                stage('Integration') {
                    steps {
                        sh 'echo Integration tests'
                    }
                }
            }
        }
    }
}
