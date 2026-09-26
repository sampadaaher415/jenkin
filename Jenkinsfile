pipeline {
    agent any

    stages {
        stage('Approve') {
            steps {
                input message: 'Deploy to production?'
            }
        }
    }
}

