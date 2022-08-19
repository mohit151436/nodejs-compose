pipeline {
  agent any  
  stages {
    stage('Build') {
      steps {
        sh 'docker build -t my-react-app .'  
        sh 'docker run -p 80:80 my-react-app:${nodejs}'
      }
    }  
  }
}
