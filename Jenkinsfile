pipeline {
 agent any
 tools {
   maven 'M2_HOME'
 
 
 }
 environment {
 registry = "tpkameni/devop-code"
 registryCredential = 'DockeruserID' 
 
 
 }
  stages {
    stage('Build' ) {
          steps {
          sh 'mvn clean'
          sh 'mvn install'
          sh 'mvn package'
        
          
          }
          
          }
    stage('Test' ) {
          steps {
          echo " test steps"
           sh 'mvn test'
   
          
          }
          
          }
    stage('deploy' ) {
          steps {
          
           script {
           docker .build registry + ":$BUILD_NUMBER"
           
           }
          
          
          }
          
          }
  
  }

}
