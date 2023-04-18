pipeline {
    agent any

    environment {
        DIRECTORY_PATH= "C:/Program Files/Jenkins"
        TESTING_ENVIRONMENT= "Aaron's Test Environment"
        PRODUCTION_ENVIRONMENT= "Aaron Sultana"
    }

    stages {
        stage('Build') {
            steps {
                echo "Fetch the source code from $DIRECTORY_PATH"
                echo "Compile the code and generate any necessary artifacts"
            }
        }
        stage('Test') {
            steps {
                echo "Unit tests"
                echo "Integration tests"
            }
        }
        stage('Code Quality Check') {
            steps {
                echo "Check the quality of the code"
            }
        }
        stage('Deploy') {
            steps {
                echo "Deploy the application to $TESTING_ENVIRONMENT"
            }
        }
        stage('Approval') {
            steps {
                sleep 10
            }
        }
        stage('Deploy to Production') {
            steps {
                echo "Deploy the application to $PRODUCTION_ENVIRONMENT"
            }
        }
    }
}