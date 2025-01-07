pipeline {
    agent any

    stages {
        stage('Hello') {
            when {
                // Only run this stage if the branch name is 'feature'
                expression { BRANCH_NAME == 'origin/feature' }
            }
            steps {
                script {
                    // Get the branch name from the Jenkins environment variable BRANCH_NAME, and print it
                    echo "Hello World from ${env.BRANCH_NAME}"
                }
            }
        }
    }
}
