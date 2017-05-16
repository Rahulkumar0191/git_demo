pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        bat 'echo "Hello"'
      }
    }
    stage ('Repo_checkout') {
      steps {
         checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/Rahulkumar0191/Test.git']]])
      }
    }  
    stage('Test') {
      steps {
        build 'Test'
      }
    }
  }
}
