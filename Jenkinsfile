pipeline {
   agent any

   stages {
      stage('Hello') {
         steps {
            echo 'Hello Deepak'
         }
      }
      
      stage('Stage2') {
         input message: 'Need your input', parameters: [string(defaultValue: '', description: '', name: 'username', trim: false)]
         steps { powershell 'write-host ${env:username}'
            
         }
      }
   }
}
