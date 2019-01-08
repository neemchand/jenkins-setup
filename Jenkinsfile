pipeline {
    agent { label 'docker' }
    environment {
        APP_VERSION = '1'
    }
    
    stages {
        stage('Build environment') {
            steps {
                echo 'Building..'
                sh 'printenv'
                sh 'echo $GIT_BRANCH'
                sh 'echo $GIT_COMMIT'
            }
        }
        stage('Test') {
            steps {
               echo 'PHP Unit tests'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying to heroku....'
            }
        }
    }
}