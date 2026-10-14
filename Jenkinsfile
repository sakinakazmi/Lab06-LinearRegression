pipeline {
    agent any

    options {
        skipDefaultCheckout(true)
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Deploy API') {
            steps {
                sh 'docker compose pull'
                sh 'docker compose up -d'
            }
        }
    }
}
