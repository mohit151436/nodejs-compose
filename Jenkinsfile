pipeline {
    parameters {
        string(name: 'nodejs', defaultValue: 'latest')
        booleanParam(name: 'dryRun', defaultValue: false)
    } 
  
  agent any  
  stages {
    stage('Build') {
      steps {
        sh 'docker build -t application_node_frontend .'
        sh 'docker tag application_node_frontend:latest application_node_frontend:${nodejs}'  
        sh 'docker run -d -it -p 3001:3000 application_node_frontend:${nodejs}'
        

      }
    }  
  }
}
