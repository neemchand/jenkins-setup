pipeline {
    agent any
    
    environment {
        APP_VERSION = '1'
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'printenv'
                sh 'echo $GIT_BRANCH'
                sh 'echo $GIT_COMMIT'
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