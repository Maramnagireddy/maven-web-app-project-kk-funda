pipeline {
    agent any

    tools {
        maven 'maven_3.9.8'  // Ensure this matches Jenkins' configured Maven name
    }

    stages {
        stage('Checkout Stage') {
            steps {
                git branch: 'development', 
                    credentialsId: '234885ab-51d5-4bb8-9f62-c6687fcfa247', 
                    url: 'https://github.com/Maramnagireddy/maven-web-app-project-kk-funda.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
                // If you're on Windows, use:
                // bat 'mvn clean package'
            }
        }
    }
}
