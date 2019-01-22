pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'mvn clean install -Dlicense.skip=true'
      }
    }
    stage('Testing') {
      parallel {
        stage('Testing') {
          steps {
            sh 'mvn sonar:sonar -Dsonar.host.url=http://13.228.25.73:8081 -Dlicense.skip=true '
          }
        }
        stage('') {
          steps {
            sh 'the tester is ${TESTER}'
          }
        }
      }
    }
  }
  tools {
    maven 'maven'
  }
}