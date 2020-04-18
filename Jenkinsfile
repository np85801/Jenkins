pipeline {
   agent any
   
   parameters {
      string (defaultValue: 'myname', description: '', name: 'test1', trim: true)
}

   stages {
      stage('Hello') {
         steps {
            echo "${$env:test1}"
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
      
      stage('stage 5')
    {
        environment {
        
                service = powershell(returnStatus: true, script: 'get-service -name ${env:test1}')
            }
            steps {
          
                powershell 'write-output "${env:service}"'
        // Success!
    }
      
                
        }
   }
   
   
}
