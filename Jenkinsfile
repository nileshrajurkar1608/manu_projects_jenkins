pipeline {
    agent any
    
    environment {
        ENV_URL = "pipeline.google.com"
    }

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }

        stage('Hai') {
            steps {
                sh '''  echo hai
                        echo hello
                        echo we are learning jenkins
                  '''
            }
        }
    }
}
