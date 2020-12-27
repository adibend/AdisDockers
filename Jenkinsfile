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
                  image 'httpd'
                }
            }
            script {
                 echo 'Building docker alpine..'
                 dockerImage = docker.build imagename
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
