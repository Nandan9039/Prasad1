
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
  stage('publish'){
  steps{
      script{
          bat ''' curl -vk -u admin:Admin1234 --upload-file target/NumberGenerator-1.0-SNAPSHOT.jar http://localhost:8082/artifactory/logic-ops-lab-libs-snapshot/ '''
      }
  }
  }
  
  }
  
}
