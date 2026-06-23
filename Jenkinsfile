pipeline {
    agent { 
        node { 

            label 'ROBOSHOP' 
        } 
    }
    stages {
        stage('Build') {
            steps {
               script{
                    sh """
                     echo "building"
                    """
               }
            }
        }
        stage('Test') {
            steps {
                 script{
                    sh """
                      echo "testing"
                    """
               }
            }
        }
        stage('Deploy') {
            steps {
              script{
                    sh """
                     echo "deploy"
                    """
               }
            }
        }
    }

     post { 
        always { 
            echo 'I will always say Hello again!'
        }
        success {
            echo "pipeline success"
        }
    }
}