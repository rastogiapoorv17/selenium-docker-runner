pipeline{
  agent any
    stages{
      stage("Start Grod){
           steps{
          sh "docker-compose up hub chrome firefox"
                          }
         }
          stage("Run Test){
           steps{
          sh "docker-compose up serch-module"
                          }
         }
         stage("Bring Grid Down"){
          steps{
          sh "docker-compose down"
          }
        }
     }
 }
