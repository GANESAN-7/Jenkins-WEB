
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out GitHub code'
            }
        }

        stage('Build') {
            steps {
                echo 'Building HTML project'
                sh 'ls -la'
            }
        }

        stage('Test') {
            steps {
                sh 'test -f index.html'
                sh 'grep -q "Welcome to Jenkins CI/CD Pipeline" index.html'
                echo 'HTML test passed'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment stage completed'
                echo 'HTML project is ready'
            }
        }
    }

    post {
        success {
            echo 'CI/CD Pipeline SUCCESS'
        }
        failure {
            echo 'CI/CD Pipeline FAILED'
        }
    }
}
