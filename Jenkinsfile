pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo "Building branch testing ${env.BRANCH_NAME}"
            }
        }
        stage('Test') {
            steps {
                echo "Running tests..."
            }
        }
    }
}
