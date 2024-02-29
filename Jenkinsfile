pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git url: 'YOUR_GIT_REPOSITORY_URL', credentialsId: 'GIT_CREDENTIALS_ID' (optional)
            }
        }
        stage('Build with Maven') {
            steps {
                withMaven(
                    maven: 'maven-3', // Replace if using a different Maven version
                    // Optional configurations (see plugin documentation for details)
                ) {
                    sh 'mvn clean verify' // Run Maven commands
                }
            }
        }
    }
}
