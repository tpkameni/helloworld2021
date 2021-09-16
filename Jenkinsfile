pipeline {
 agent any
 tools {
   maven 'M2@HOME'
 
 
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
          echo " deploy steps"
          sleep 10
          
          }
          
          }
    stage("docker" ) {
          steps {
          echo " image steps"
          sleep 10
          
          }
          
          }
  }

}
