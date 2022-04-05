def version = "1.0.0-release"
def artifactId ="demo-app"
def groupId = "com.siemens.devops"
def appName = "demo-app"
def JfrogUrl ="http://localhost:8082/artifactory/logic-ops-lab-libs-release/"



pipeline {
     agent any
  stages {

   
        
   stage('mvnBuild'){
      steps{
      script{
      bat ''' mvn clean package sonar:sonar -Dsonar.host.url=http://localhost:8084 -Dsonar.login=4067d5a7602fb1fd711908d27859014eb816a4b6 -Dsonar.projectKey=first '''
      
            }
      }
  }
  
  }
  
}
