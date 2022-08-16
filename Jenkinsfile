pipeline {
    parameters {
        string(name: 'nodejs', defaultValue: 'latest')
        booleanParam(name: 'dryRun', defaultValue: false)
    } 
  
  agent any   
  stages {    
    stage('Build') {
      steps {
        sh 'npm install'
        sh 'docker tag application_node_frontend:latest application_node_frontend:${nodejs}'

      }
    }  
  }
}
