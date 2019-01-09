pipeline {
    agent {  docker { image 'bitnami/laravel'}
                } 
    
    environment {
        APP_VERSION = '1'
    }
    stages {
        stage('Build') {
            steps {
                   sh 'php --version'
                   sh 'composer install'
            }
        }
        stage('Test') {
            steps {
                echo 'test Done...2.'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
            post {
                always {
                    echo 'Deploying..1.'
                }

                success {
                    echo 'Deploying ...2.'
                }

                failure {
                    echo 'Deploying...3.'
                }
              }
        }
    }
    post {
        always {
          echo 'test Done...1.'
      }

      success {
          echo 'test ...2.'
      }

      failure {
          echo 'test Done...3.'
      }
    }
}