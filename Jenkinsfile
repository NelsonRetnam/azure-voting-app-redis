pipeline {
   agent any

    environment {
      PATH = "C:\\WINDOWS\\SYSTEM32;C:\\Program Files\\Git\\bin;C:\\Program Files\\nodejs\\;C:\\Users\\USER_NAME\\AppData\\Roaming\\npm;C:\Program Files\PowerShell\7"
   }

   stages {
      stage('Verify Branch1') {
         steps {
            echo "$GIT_BRANCH"
         }
      }
      stage('Docker Build') {
         steps {
            pwsh 'docker images -a'
            // sh """ 
            //    cd azure-vote/
            //    docker images -a
            //    docker build -t jenkins-pipeline .
            //    docker images -a
            //    cd ...
            // """
         }
      }
   }
}

