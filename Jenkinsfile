pipeline {
    agent any
    stages {
          stage ('Compile Stage') {                
                steps {
                    withMaven(maven : 'maven-3') {
                      sh 'mvn clean compile'
                 }
              }
        
         }
          stage ('Testing Stage') {             
              step {
                  withMaven(maven : 'maven-3') {
                      sh 'mvn test'
                    }
              }
          }
           
            stage ('Deploying Stage') {             
                 step {
                    withMaven(maven : 'maven-3') {
                      sh 'mvn deploy'
                    }
                 }
            }
        }
          
  }   
