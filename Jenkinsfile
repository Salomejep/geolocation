pipeline{
    agent any
    tools{
     maven 'M2_HOME'
    }
    stages{
        stage('sonar-scan'){
            steps{
              sh 'mvn verify org.sonarsource.scanner.maven:sonar-maven-plugin:sonar -Dsonar.projectKey=Salomejep_geolocation'
            }
        }
    }
}