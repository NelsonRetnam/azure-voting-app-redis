pipeline {
   agent any

   stages {
      stage('Verify Branch1') {
         steps {
            echo "$GIT_BRANCH"
         }
      }
      stage('Docker Build') {
         steps {
            pwsh 'docker images -a'
            pwsh """ 
               cd azure-vote/
               docker images -a
               docker build -t jenkins-pipeline .
               docker images -a
               cd ...
            """
         }
      }
   }
}
