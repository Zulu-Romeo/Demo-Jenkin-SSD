pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                // Here you can define commands for your build
            }
        }
        stage('Test') {
            when {
                // Define your condition here
                expression { 
                    // Add your condition logic
                    // For example:
                    return env.RUN_TESTS == 'true'
                }
            }
            steps {
                echo 'Testing..'
                // Here you can define commands for your tests
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                // Here you can define commands for your deployment
            }
        }
    }
    post {
        success {
            echo 'Pipeline executed successfully! Sending notifications...'
            // Add actions for successful pipeline execution, like sending notifications
        }
        failure {
            echo 'Pipeline failed! Notifying stakeholders...'
            // Add actions for failed pipeline execution, like notifying stakeholders
        }
        always {
            echo 'Cleaning up...'
            // Add actions that should always run regardless of pipeline status
        }
    }
}
