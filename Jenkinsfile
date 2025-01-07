pipeline {
    agent any

    stages {
        stage('Hello') {
            when {
                expression { env.GIT_BRANCH == 'origin/feature' }
            }
            steps {   
                    withSonarQubeEnv(installationName: 'sq1') { 
                    sh "./mvnw clean verify sonar:sonar -Dsonar.projectKey=branch-test-analysis -Dsonar.projectName='branch-test-analysis'"
                }
            }
        }
    }
}


