pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo "Running build..."
                sh "echo building..."
            }
        }

        stage('Test') {
            steps {
                echo "Running tests..."
                sh "echo tests passed"
            }
        }

        stage('Deploy to Testing') {
            when {
                branch 'develop'
            }
            steps {
                echo "Deploying to TESTING server..."
                sh "echo deployed to testing"
            }
        }

        stage('Deploy to Production') {
            when {
                branch 'main'
            }
            steps {
                echo "Deploying to PRODUCTION server..."
                sh "echo deployed to production"
            }
        }
    }
}
