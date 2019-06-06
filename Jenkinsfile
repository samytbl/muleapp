pipeline {
  agent any
  stages {
    stage('Unit Test') { 
      steps {
        sh 'mvn clean test'
      }
    }
    stage('Deploy Standalone') { 
      steps {
        sh 'mvn deploy -P standalone'
      }
    }
    stage('Deploy Cloudhub INT') { 
      steps {
        sh 'mvn deploy -DmuleDeploy -Dcloud.env=INT -DcloudhubAppName=stime-poc -Dmule.version=4.2.0 -Dcloud.user=samy_toubal -Dcloud.password=\'Bon2jour!Aloha\''      	
      }
    }
  }
}