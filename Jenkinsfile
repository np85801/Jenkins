pipeline {
   agent any

   stages {
      stage('Hello') {
         steps {
            echo 'Hello Deepak'
         }
      }
      
      stage('Stage2') {
         input{
        message "Press Ok to continue"
        submitter "user1,user2"
        parameters {
            string(name:'username', defaultValue: 'user', description: 'Username of the user pressing Ok')
        }
        
        }
         steps { powershell 'write-host ${env:username}'
            
         }
      }
   }
}
