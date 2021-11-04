pipeline {
   agent any

    stages {
      stage('Verify Branch') {
         steps {
            echo "$GIT_BRANCH"
            powershell 'write-output "hello"'
         }
      }
   }
}
