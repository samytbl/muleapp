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
    //deploy test
    stage('Deploy Cloudhub INT') { 
      steps {
        sh 'mvn deploy -DmuleDeploy -Dcloud.env=INT -DcloudhubAppName=mule-cicd-test-dev -Dmule.version=4.1.4 -Dcloud.user=samy_toubal -Dcloud.password=\'Bon2jour!Aloha\''
      }
    }
  }
}
