pipeline {
    agent any

    stages {
        stage('Debug') {
            steps {
                script {
                    echo "Current branch name: ${env.BRANCH_NAME}"
                    // If BRANCH_NAME is null, try checking other variables that might give clues
                    echo "Full ref: ${env.GIT_BRANCH}"
                    echo "Commit ID: ${env.GIT_COMMIT}"
                }
            }
        }
        stage('Hello') {
            when {
                expression { env.BRANCH_NAME == 'feature' }
            }
            steps {
                script {
                    echo "Hello World from ${env.BRANCH_NAME}"
                }
            }
        }
    }
}
