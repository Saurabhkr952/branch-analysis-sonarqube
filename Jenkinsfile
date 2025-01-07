pipeline {
    agent any

    stages {
        stage('Sonar Scan') {
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
    }
}


