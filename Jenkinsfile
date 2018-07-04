pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}"
                checkout scm
            }
        }
        stage('Install dependencies') {
            steps {
                sh "export PIPENV_VENV_IN_PROJECT"
                sh "/usr/local/bin/pip3.7 install pipenv"
                sh "/usr/local/bin/pipenv install --verbose --three"
            }
        }
        stage('Tests') {
            steps {
                echo "Running tests..."
            }
        }
    }
}