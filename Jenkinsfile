pipeline {
  agent any
  stages {
    stage('Main_Repo') {
      steps {
        bat 'echo "Hello"'
      }
    }
    stage ('Repo_checkout') {
      steps {
         checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/Rahulkumar0191/Test.git']]])
      }
    }  
      stage ('Build') {
      steps {
         powerShell('Write-Output "Hello World!"')
      }
    }
    stage('Test') {
      steps {
        build 'Test'
      }
    }
  }
}
