pipeline {
    agent { node { label "docker" }}

    stages {
        stage('Build') {
            steps {
                echo 'Building docker alpine..'
                docker run alpine echo "Hello World"
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
