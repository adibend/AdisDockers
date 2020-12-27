pipeline {
    agent { node { label "docker" }}

    stages {
        stage('Build') {
            
             agent {
                docker {
                  label 'docker'  // both label and image
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
