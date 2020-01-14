pipeline {
   agent any

   stages {
      stage('Hello') {
         steps {
           if (env.BRANCH_NAME == 'develop') {
            echo 'Hello Develop'
           } else {
             echo 'Hello Master'
           }
         }
      }
   }
}
