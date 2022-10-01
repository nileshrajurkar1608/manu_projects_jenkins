pipeline {
    agent { 
        label 'ANSIBLE' 
        } 
    stages {
        stage('Parallel') {
            parallel {
                stage('One') {
                    steps {
                        sh "hostname"
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
        success {
            cleanWs()
        }
    }
}