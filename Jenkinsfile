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
        stage('Approve') {
            when {
                expression {
                    params.Environment == 'production'
                }
            }

            steps {
                input message: 'Deploy to production?'
            }
        }
    }

    post {
        success {
            echo 'Pipeline succeeded'
        }

        failure {
            echo 'Pipeline failed'
        }
    }
}
