pipeline {
	agent any
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