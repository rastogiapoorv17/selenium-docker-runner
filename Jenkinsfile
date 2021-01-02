pipeline{
  agent any
    stages{
      stage("Pulls Latest Image){
           steps{
          sh "docker pull rastogiapoorv/seleniumdocker"
                          }
         }
      stage("Start Grid){
           steps{
          sh "docker-compose up -d hub chrome firefox"
                          }
         }
          stage("Run Test){
           steps{
          sh "docker-compose up search-module"
                          }
         }
         
     }
                post{
                  always{
                    archieveArtifacts artifacts: 'output/**'
                      sh "docker-compose down"
                  }
                } 
               
 }
