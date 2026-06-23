pipeline {
    agent { 
        node { 

            label 'ROBOSHOP' 
        } 
    }

     environment {
            COURSE="jenkins"
        }
    options { 
        disableConcurrentBuilds() 
        }
    stages {
        stage('Build') {
            steps {
               script{
                    sh """
                     echo "building"
                     echo $COURSE
                     sleep 5
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
        failure {
            echo "pipeline failure"
        }
    }
}