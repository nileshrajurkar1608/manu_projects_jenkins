pipeline {
    agent any 
    stages {
        stage('Parallel') {
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
    post {
        unstable {
            cleanWs()
        }
    }
}