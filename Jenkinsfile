pipeline{
  agent any
    stages{
      stage("Start Grod){
           steps{
          sh "docker-compose up -d hub chrome firefox"
                          }
         }
          stage("Run Test){
           steps{
          sh "docker-compose up search-module"
                          }
         }
         stage("Bring Grid Down"){
          steps{
          sh "docker-compose down"
          }
        }
     }
 }
