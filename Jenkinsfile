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
         
     }
                post{
                  always{
                    archieveArtifacts artifacts: 'output/**'
                      sh "docker-compose down"
                  }
                } 
               
 }
