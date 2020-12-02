 
pipeline {
    
    agent any
 
    tools {
        maven "Maven"
    }
  
    stages {   
        stage('Test') {
            steps { 
              echo 'Testing the Application'
              sh 'mvn test'
            }
        }
     
        stage('Build') {
            steps {
              echo 'Deploying the Application'
              sh 'mvn package'
            }
        }

    }
}
