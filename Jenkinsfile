pipeline {
   agent any

   stages {
      stage('Hello') {
         steps {
            echo 'Hello Dinesh'
         }
      }
      
      stage('Stage2') {
         steps {
            powershell label: 'test', script: 'write-host "this is my pieline SCM Test"'
         }
      }
   }
}
