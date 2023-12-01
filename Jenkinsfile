pipeline {
    agent any
    environment {
        VERSION = "2.2.4"
    }

    stages {
        stage('Build') {
            steps {
                echo "Building... with version ${env.VERSION}"
                // Add your build commands here
            }
        }

        stage('Test') {
            when {
                expression {
                    // Modify conditions as needed
                    return params.flag == false || params.flag == true
                }
            }
            steps {
                // Add test steps here
                echo 'Testing...'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying...'
                // Add your deployment commands here
            }
        }
    }
    
    post {
        always {
            echo 'This will always run, regardless of the build result'
            // Add any post-build actions that should always run here
        }
        failure {
            echo 'This will run only if the build fails'
            // Add any post-build actions specific to failure here
        }
    }
}
