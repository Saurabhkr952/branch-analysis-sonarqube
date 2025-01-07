pipeline {
    agent any

    stages {
        
         stage('Branch name') {
            steps {   
            echo "Branch: ${env.GIT_BRANCH}"
            }
        }
        
        stage('Sonar Scan feature branch') {
            when {
                expression { env.GIT_BRANCH == 'origin/feature' }
            }
            steps {   
                    withSonarQubeEnv(installationName: 'sq1') { 
                        sh 'chmod +x mvnw'
                        sh "./mvnw clean sonar:sonar -Dsonar.projectKey=branch-test-analysis -Dsonar.projectName='branch-test-analysis'"
        //              sh './mvnw clean org.sonarsource.scanner.maven:sonar-maven-plugin:3.9.0.2155:sonar'     # uses jenkins sonarqube plugins
                }
            }
        }
    }
}
