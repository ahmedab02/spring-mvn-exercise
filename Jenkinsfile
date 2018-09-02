 pipeline {
       agent {
       node {
          label 'linux'
          
       }
     } 
  environment {
   def  mvnHome = tool 'M3'
  }
  stages {
   
     
   
   stage('checkout') {
            steps {
              checkout scm
            }
          }
    
    stage('build') {
     steps {
       
         sh "${mvnHome}/bin/mvn build "
      }
    }
    
    stage('test') {
     steps {
    
         sh "${mvnHome}/bin/mvn test "
      }
    }
   


  }
}
