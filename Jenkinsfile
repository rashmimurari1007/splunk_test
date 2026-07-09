pipeline {
    agent any

    options {
        timestamps()
    }

    stages {
        stage('Show Context') {
            steps {
                echo "Branch: ${env.BRANCH_NAME}"
                echo "Job: ${env.JOB_NAME}"
                echo "Build: ${env.BUILD_NUMBER}"
                echo "Change ID: ${env.CHANGE_ID}"
                echo "Change Branch: ${env.CHANGE_BRANCH}"
                echo "Change Target: ${env.CHANGE_TARGET}"
            }
        }

        stage('Build') {
            steps {
                echo "Running build for ${env.BRANCH_NAME}"
            }
        }

        stage('Test') {
            steps {
                echo "Running test stage"
            }
        }
    }

    post {
        success {
            echo "Pipeline succeeded"
        }
        failure {
            echo "Pipeline failed"
        }
    }
}
