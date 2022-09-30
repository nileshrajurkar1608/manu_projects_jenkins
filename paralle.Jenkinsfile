pipeline {
    agent any 
    stages {
        stage('Paraller') {
            parallel {
                stage('One') {
                    steps {
                        echo "sleep 30"
                    }
                }

                stage('Two') {
                    steps {
                        echo "sleep 30"
                    }
                }

                stage('Three') {
                    steps {
                        echo "sleep 30"
                    }
                }
            }
        }
    }
}