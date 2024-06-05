pipeline {
    agent any
    
    triggers {
        pollSCM('* * * * *') // Polls the SCM every minute. Adjust as needed.
    }

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from the repository
                checkout scm
            }
        }

        stage('Build') {
            steps {
                script {
                    // No build step for a static HTML, CSS, JS project
                    echo 'Build step - Nothing to build for static site'
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    // You can add steps to deploy your static site
                    // For example, you might copy files to a web server
                    echo 'Deploy step - Add your deployment script here'
                }
            }
        }
    }

    post {
        success {
            echo 'Build succeeded'
        }
        failure {
            echo 'Build failed'
        }
    }
}