pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        bat 'echo "Hello"'
      }
    }
    stage('Test') {
      steps {
        build 'Test'
      }
    }
  }
}