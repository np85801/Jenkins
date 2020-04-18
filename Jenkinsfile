pipeline {
   agent any
   
   parameters {
      string (defaultValue: 'myname', description: '', name: 'test1', trim: true)
}

   stages {
      stage('Hello') {
         steps {
            echo "${$env:name}"
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
