pipeline {
    agent any

    stages {
        stage('Hello') {
            when {
                expression { env.GIT_BRANCH == 'origin/feature' }
            }
            steps {
                script {
                    echo "Hello World from ${env.GIT_BRANCH}"
                }
            }
        }
    }
}

