pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'mvn clean install -Dlicense.skip=true'
      }
    }
    stage('Testing') {
      steps {
        sh 'mvn sonar:sonar -Dsonar.host.url=http://13.228.25.73:8081 -Dlicense.skip=true '
      }
    }
  }
  tools {
    maven 'maven'
  }
}