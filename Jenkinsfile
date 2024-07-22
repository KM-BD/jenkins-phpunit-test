pipeline {
    agent {
        docker {
            image 'composer:latest'
            args '-v /var/run/docker.sock:/var/run/docker.sock'
        }
    }
    environment {
        DOCKER_HOST = 'tcp://host.docker.internal:2375'
    }
    stages {
        stage('Build') {
            steps {
                sh 'composer install'
            }
        }
        stage('Test') {
            steps {
                sh './vendor/bin/phpunit tests'
            }
        }
    }
}
