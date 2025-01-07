pipeline {
    agent any

    stages {
        stage('Sonar Scan feature branch') {
            when {
                expression { env.GIT_BRANCH == 'origin/feature' }
            }
            steps {   
                    withSonarQubeEnv(installationName: 'sq1') { 
                        sh 'chmod +x mvnw'
                        sh "./mvnw clean sonar:sonar -Dsonar.projectKey=branch-test-analysis -Dsonar.projectName='branch-test-analysis'"
                }
            }
        }
        stage('Sonar Scan prod branch') {
            when {
                // Only run this stage if the branch name is 'feature'
                expression { env.BRANCH_NAME == 'feature' }
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
