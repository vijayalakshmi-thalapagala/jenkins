pipeline {
    agent {
        node {
            label 'roboshop'
        }
    }
    stages { 
        stage('Build') {
            steps {
                script {
                    sh """
                        echo "Building"
                        exit 1
                    """
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    sh """
                        echo "Testing"
                    """
                }    
            }
        }
        stage('Deploy') {
            steps {
                script {
                    sh """
                        echo "Deploying"
                    """
                }
            }
        }
    }
    //post Build
    post {
        always {
            echo "I will always say Hello world"
        }
        success {
            echo "pipeline success"
        }
        failure {
            echo "pipeline failure"
        }
    }
}