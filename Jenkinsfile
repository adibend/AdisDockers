pipeline {
    
    environment {
            imagename = "httpd"
            dockerImage = ''
            }
    agent { node { label "LinuxSlave" }}

    stages {
        stage('Build') {
            
             agent {
                docker {
                  label 'LinuxSlave'   
                  image 'maven:3.5-alpine'
                }
            }
            steps {
                 echo 'Building docker alpine..'
                 sh 'mvn --version'
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
