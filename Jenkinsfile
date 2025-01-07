pipeline {
    agent any

    stages {
        stage('Debug') {
            steps {
                script {
                    echo "Current branch name: ${env.BRANCH_NAME}"
                }
            }
        }
        stage('Hello') {
            when {
                expression { env.BRANCH_NAME == 'origin/feature' }
            }
            steps {
                script {
                    echo "Hello World from ${env.BRANCH_NAME}"
                }
            }
        }
    }
}
