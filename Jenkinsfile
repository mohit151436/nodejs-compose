pipeline {
    parameters {
        string(name: 'nodejs', defaultValue: 'latest')
        booleanParam(name: 'dryRun', defaultValue: false)
    } 
  
  agent any  
  stages {
    stage('Build') {
      steps {
        sh 'docker build -t my-react-app .'
        sh 'docker tag my-react-app:latest my-react-app:${nodejs}'  
        sh 'docker run -p 80:80 my-react-app:${nodejs}'
        

      }
    }  
  }
}
