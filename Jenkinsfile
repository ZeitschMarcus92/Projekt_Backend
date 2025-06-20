pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                dir('Projekt_Backend') {
                    sh './mvnw clean install'
                }
            }
        }

        stage('Test') {
            steps {
                dir('Projekt_Backend') {
                    sh './mvnw test'
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Hier erfolgt das Deployment'
            }
        }
    }
}