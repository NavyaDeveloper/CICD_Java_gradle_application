pipeline{
    agent any
    stages{
        stage("Sonar Quality Check"){
           
            steps{
                script {
                    withSonarQubeEnv(credentialsId: 'token') {
                        sh 'chmod +x gradlew'
                        sh './gradlew sonarqube'
                   }
                }
            }
        }
    }
}