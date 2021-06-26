pipeline
 {
  agent any
  stages{
   stage{'Build Applicaion'}{
   steps{
   bat 'mvn clean install'
   }
   }
   
   stage{'Dploy Applicaion To Mulesoft Cloudhub'}{
   steps{
   bat 'mvn package deploy -DmuleDeploy' 
   } 
   }
   
   stage{'Perform Regression Testing'}{
   steps{
   bat 'newman run C:\\Users\\shani\\newman\\NationalRailNJCAuthenticationSapi.postman_collection.json --disable-unicode' 

   }
   }
 
 }
 }