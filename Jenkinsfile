pipeline {
    agent any
    
    environment {
        APP_VERSION = '1'
    }
    stages {
        stage('Build') {
            agent {
                    docker { image 'php'}
                   }    
            steps {
                   sh 'php --version'
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