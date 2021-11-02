pipeline {
   agent any

   stages {
      stage('Verify Branch1') {
         steps {
            echo "$GIT_BRANCH"
         }
      }
   }
   stages {
      stage('Docker Build') {
         steps {
            pwsh(script: 'docker images -a')
            pwsh(script: """ 
               cd azure-vote/
               docker images -a
               docker build -t jenkins-pipeline .
               docker images -a
               cd ...
            """)
         }
      }
   }
}
