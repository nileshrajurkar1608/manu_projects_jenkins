pipeline {
    agent any
    environment {
        ENV_URL     = "pipeline.google.com"
        SSH_CRED    = credentials('SSH')
    }
    
    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }

    triggers {
            pollSCM('*/2 * * * *')
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
                sh "env"
            }

        }
    }
}
// environment variable for ssh username and pass
// SSH_CRED_USR
// SSH_CRED_PSW
// some changes