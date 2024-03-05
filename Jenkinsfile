pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                // TODO: Build the application
                sh './gradlew assemble'
            }
        }
        stage('Test') {
            steps {
                // TODO: Run tests
                sh './gradlew test'
            }
        }
    }
    
    post {
        success {
            echo 'Pipeline succeeded! Deploying...'
            // Add deployment steps here
        }
        failure {
            echo 'Pipeline failed! Notify team...'
            // Add notification or rollback steps here
        }
    }
}
