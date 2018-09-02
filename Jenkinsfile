 pipeline {
       agent {
       node {
          label 'linux'
          
       }
     } 
     
  stages {
   
        environment {
    mvnHome = tool 'M3'
  }
   
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
