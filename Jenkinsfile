pipeline {
    agent any
    environment {
        ENV_URL = "pipeline.google.com"
    }

    stages {
        stage('variable') {
            steps {
                sh "echo ${ENV_URL}"  
            }
        }

        stage('Hai') {
            steps {
                sh "echo hai"
                sh "echo Environment URL is ${ENV_URL}"
            }

        }
    }
}