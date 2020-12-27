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
            steps {
                 echo 'Building docker alpine..'
                 docker.image('httpd').withRun('-i -t --name nicehttpd -p 8080:80 httpd')
                
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
