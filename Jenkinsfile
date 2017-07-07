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
         input 'Confirm'
         bat 'powershell "Copy-Item -Path D:\Azure\output\* -Destination D:\svn_poc\cop\ -force"'
      }
    }
    stage('Test') {
      steps {
        build 'Test'
      }
    }
  }
}
