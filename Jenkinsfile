pipeline {
    agent any  // Use any available agent
    stages {
        stage('Checkout') {
            steps {
               checkout scm
            }
        }

        stage('Compile') {
            steps {
                // Compile the Java program
                script {
                    sh 'javac WelcomeMessage.java'
                }
            }
        }

        stage('Run') {
            steps {
                // Run the Java program
                script {
                    sh 'java WelcomeMessage'
                }
            }
        }
    }

    post {
        success {
            echo 'Java program ran successfully!'
        }
        failure {
            echo 'Java program failed.'
        }
    }
}
