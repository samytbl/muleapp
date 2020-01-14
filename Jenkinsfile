pipeline {
   agent any

   stages {
      stage('Hello') {
         steps {
           if (env.BRANCH_NAME == 'master') {
            echo 'Hello Master'
           } 
         }
      }
   }
}
