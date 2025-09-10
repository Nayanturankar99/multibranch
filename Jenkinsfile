pipeline {
    agent any

    environment {
        APP_NAME = "TestApp"
    }

    stages {
        stage('Checkout') {
            steps {
                echo "Checking out the code..."
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo "Building ${env.APP_NAME}..."
                // Example build step; replace with your real build commands
                sh 'echo "Compiling source code..."'
            }
        }

        stage('Test') {
            steps {
                echo "Running tests..."
                // Example test step; replace with actual test commands
                sh 'echo "Tests passed successfully!"'
            }
        }

        stage('Deploy') {
            when {
                branch 'main'
            }
            steps {
                echo "Deploying ${env.APP_NAME} as this is the main branch..."
                // Example deploy step; replace with actual deployment logic
                sh 'echo "Deployment complete!"'
            }
        }
    }

    post {
        always {
            echo "This pipeline has finished, regardless of the result."
        }
        success {
            echo "Build and tests completed successfully!"
        }
        failure {
            echo "Something went wrong. Please check the logs!"
        }
    }
}
