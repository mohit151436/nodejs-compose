pipeline {
  agent any
  parameters {
    imageTag(name: 'DOCKER_IMAGE', description: '',
             image: 'jenkins/jenkins', filter: 'lts.*', defaultTag: 'lts-jdk11',
             registry: 'https://registry-1.docker.io', credentialId: '', tagOrder: 'NATURAL')
  tools {nodejs "node"}
  stages {
    stage('Build') {
      steps {
        sh 'docker-compose -f docker-compose.yaml up -d'
      }}}}
