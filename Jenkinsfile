pipeline {
   agent any

   stages {
      stage('Hello') {
         steps {
            echo 'Hello Deepak'
         }
      }
      
      stage('Stage2') {
         steps {
            input message: 'Need your input', parameters: [string(defaultValue: '', description: '', name: 'username', trim: false)]
         }
      }
   }
}
