pipeline {
    parameters {
        string(name: 'nodejs', defaultValue: 'latest')
        booleanParam(name: 'dryRun', defaultValue: false)
    } 
  
  agent any
    
  tools {nodejs "node"}
    
  stages {
        
    stage('Git') {
      steps {
        git 'https://github.com/mohit151436/nodejs-compose.git'
      }
    }
     
    stage('Build') {
      steps {
        sh 'npm install'
        sh 'docker run -d -it -p 3000:3000 application_node_frontend:latest'
        sh 'docker tag application_node_frontend:latest application_node_frontend:${nodejs}'

      }
    }  
              
    stage('Test') {
      steps {
        sh 'node test'
      }
    }
  }
}
