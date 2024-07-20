pipeline {
    agent any
    environment {
        DOCKER_HOST = 'tcp://docker:2376'
        DOCKER_CERT_PATH = '/certs/client'
        DOCKER_TLS_VERIFY = '1'
    }
    stages {
        stage('Build') {
            steps {
                script {
                    sh 'docker --version'
                    sh 'docker ps'
                    sh 'docker pull composer:latest'
                }
            }
        }
    }
}
