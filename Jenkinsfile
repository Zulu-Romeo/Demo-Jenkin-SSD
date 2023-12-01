pipeline {
    agent any
    environment {
        VERSION = "2.2.4"
    }

    stages {
        stage('Build') {
            steps {
                echo "Building... with version ${VERSION}"
                echo 'Building...'
                // Add your build commands here
            }
        }

        stage('Test') {
            when {
                expression {
                    return flag == false
                    return flag == true
                }
            }
            steps {
@@ -27,7 +25,7 @@ pipeline {

        stage('Deploy') {
            steps {
                echo 'Deploying... And test stage should be skipped'
                echo 'Deploying...'
                // Add your deployment commands here
            }
        }
