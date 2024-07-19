pipeline {
    agent {
        docker {
            image 'composer:latest'
            label 'docker-agent' // Optional: specify if you have labeled nodes
        }
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
