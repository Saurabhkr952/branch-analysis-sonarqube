pipeline {
    agent any

    stages {
        stage('Hello') {
            when {
                expression { env.GIT_BRANCH == 'origin/feature' }
            }
            steps {   
                    withSonarQubeEnv(installationName: 'sq1') { 
                    def mvn = tool 'Default Maven';    
                    sh "${mvn}/bin/mvn clean verify sonar:sonar -Dsonar.projectKey=branch-test-analysis -Dsonar.projectName='branch-test-analysis'"
                }
            }
        }
    }
}


