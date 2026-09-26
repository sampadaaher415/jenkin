pipeline {
  agent any
  parameters {
      choice(name: 'Environment', choices: ['staging', 'production'], description: ''Target)
  }
   stages { 
     stage('Deploy') {
          steps {
               sh "echo Deploying to ${params.ENVIRONMENT}"
      }
    }
  }
}
