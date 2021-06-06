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
    sh 'mv target/maven*.war target/myweb.war'
    withSonarQubeEnv(credentialsId: 'sonar7-token') {
    // some block
       sh 'mvn sonar:sonar'
}
  
   }
  }
        }
        }
