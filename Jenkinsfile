pipeline {
 agent any
 tools {
  maven  'maven3'
 }
 
 stages{
  stage("Maven Build"){
        steps{
         sh 'mvn clean package'
        }
        }
  stage("Sonar Qube Analysis"){
   steps{
    script{
    withSonarQubeEnv(credentialsId: 'sonar7-token') {
    // some block
       sh 'mvn sonar:sonar'
}
    }
  
   }
  }
        }
        }
