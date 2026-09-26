pipeline {
    agent any

    parameters {
        choice(
            name: 'Environment',
            choices: ['staging', 'production'],
            description: 'Target'
        )
    }

    stages {
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
