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
                expression { env.GIT_BRANCH == 'origin/prod' }
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


