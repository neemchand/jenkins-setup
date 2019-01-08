pipeline {
    agent any
    
    environment {
        APP_VERSION = '1'
    }
    stages {
        stage('Build') {
            steps {
               agent {
                    docker {
                            image 'php'
                        }
                     }
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}