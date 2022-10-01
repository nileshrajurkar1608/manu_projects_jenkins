pipeline {
    agent any
    environment {
        ENV_URL = "pipeline.google.com"
    }

    stages {
        stage('variable') {
            steps {
                sh "echo Global variable is ${ENV_URL}"  
            }
        }

        stage('Hai') {
            environment {
                ENV_URL = "stage.google.com"
            }
            steps {
                sh "echo hai"
                sh "echo Local variable is ${ENV_URL}"
            }

        }
    }
}