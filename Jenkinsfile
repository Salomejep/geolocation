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
        stage("maven"){
        steps{ 
        sh 'mvn clean validate compile install test package'
        }
    }
}