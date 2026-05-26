pipeline {
    agent {
        node {
            label 'roboshop'
        }
    }
    environment {
        COURSE = jenkins
    }
    options {
        disableConcurrentBuilds()
    }
    stages { 
        stage('Build') {
            steps {
                script {
                    sh """
                        echo "Building"
                        echo $COURSE
                        sleep 10
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