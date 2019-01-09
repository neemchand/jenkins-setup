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
                echo 'run unit test'
            }
        }
        stage('Deploy to UAT') {
            steps {
                echo 'Deploying to uat....'
            script {
                    sshagent(['ci-ssh']) {
                        sh """
                            git push origin heroku master"
                        """
                    }
            }        
            }
            post {
                success {

                    echo 'Deployment to uat success'
                }

                failure {
                    echo 'Deployment to uat fails'
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
          echo 'failure'
      }
    }
}