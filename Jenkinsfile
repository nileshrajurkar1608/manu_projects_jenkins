pipeline {
    agent any    
    environment {
        ENV_URL       = "pipeline.google.com"
        SSH_CRED      = credentials('SSH')
    }

    stages {
        stage('Hai') {
            steps {
                sh "echo ${ENV_URL} "  
                    
            }
        }

        stage('Hello') {
            environment {
                ENV_URL = "stage.google.com"
            }
            steps {
                 sh "echo hai"  
                 sh "echo Environment URL is ${ENV_URL}"
                 sh "env" 
            }
        }
    }
}
