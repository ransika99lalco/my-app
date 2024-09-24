pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the Application...'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing the Application ...'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying the Application...'
            }
        }
        stage('Check React Version') {
            steps {
                script {
                    // Check for React version
                    def packageJson = readJSON file: 'package.json'
                    def reactVersion = packageJson.dependencies.react ?: 'Not found'
                    echo "React version: ${reactVersion}"
                }
            }
        }
    }
    post {
        Success {
            echo 'Application Build Successfully...'
        }
    }
}
