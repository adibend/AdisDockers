pipeline {
    agent { node { label "LinuxSlave" }}

    stages {
        stage('Build') {
            
             agent {
                docker {
                  image 'maven:3-alpine'
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
