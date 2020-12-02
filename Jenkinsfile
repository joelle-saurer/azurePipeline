 
pipeline {
    
    agent any
 
    tools {
        maven "Maven"
    }
  
    stages {
        stage("Clone code from VCS") {
            steps {
                script {
                    git clone 'https://github.com/joelle-saurer/DevOps-Challenges.git';
                }
            }
        }
        
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
