pipeline {
   agent any

   stages {
      stage('Example (Not master)') {
         when {
            not {
               branch 'develop'
            }
         }
         steps {
               echo 'HELLO WORLD'
          }
       }
    }
}
