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
        // choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
        // password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }

    triggers {
            pollSCM('*/2 * * * *')
        }
    tools {
        maven 'maven-3.8.5' 
    }

    stages {
        stage('variable') {
            steps {
                sh "echo Global variable is ${ENV_URL}"  
            }
        }

        stage('Hai') {
            when { branch 'main' }            
            environment {
                ENV_URL = "stage.google.com"
            }
            input {
                message "Should we continue?"
                ok "Yes, we should."
                submitter "alice,bob"
                parameters {
                    string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
                }
            }
            steps {
                sh "echo hai"
                sh "echo Local variable is ${ENV_URL}"
                sh "env"
                sh "echo I will be running maven command"
                sh "mvn -v"
            }

        }
    }
}
// environment variable for ssh username and pass
// SSH_CRED_USR
// SSH_CRED_PSW
// some changes
//next changes