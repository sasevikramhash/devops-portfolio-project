pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Validate files') {
            steps {
                sh '''
                    test -f index.html
                    test -f style.css
                '''
            }
        }

        stage('Test HTML content') {
            steps {
                sh '''
                    grep -q '<html' index.html
                    grep -q 'stylesheet' index.html
                    grep -q 'style.css' index.html
                '''
            }
        }

        stage('Package website') {
            steps {
                sh '''
                    mkdir -p dist
                    cp index.html style.css dist/
                '''
            }
        }
    }

    post {
        success {
            echo 'Website validation and packaging completed successfully!'
        }
        failure {
            echo 'Pipeline failed. Check the console output.'
        }
        always {
            echo 'Pipeline execution finished.'
        }
    }
}
