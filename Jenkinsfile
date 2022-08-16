pipeline {
    parameters {
        string(name: 'nodejs', defaultValue: 'latest')
        booleanParam(name: 'dryRun', defaultValue: false)
    }             
  agent any
  tools {nodejs "node"}
  stages {
    stage('Build') {
      steps {
        sh 'docker tag nodejs_frontend:latest nodejs_frontend:${nodejs}'
        sh 'docker-compose -f docker-compose.yaml up -d'
      }}}}
