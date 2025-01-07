pipeline {
    agent any

    stages {
        stage('Hello') {
            when {
                expression { env.GIT_BRANCH == 'origin/feature' }
            }
            steps {   
                    withSonarQubeEnv(installationName: 'sq1') { 
                    sh 'mvn clean org.sonarsource.scanner.maven:sonar-maven-plugin:3.9.0.2155:sonar'
                }
            }
        }
    }
}


