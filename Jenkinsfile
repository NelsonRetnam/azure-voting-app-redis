pipeline {
   agent any

    stages {
      stage('Verify Branch') {
         steps {            
            echo "$GIT_BRANCH"
            echo env.BRANCH_NAME
         }
      }
      stage('Docker Build') {
         steps {
            sh 'pwd'
            sh 'docker images -a'
            sh """ 
               cd azure-vote/
               docker images -a .
               docker build -t jenkins-pipeline .
               docker images -a
               cd ..
            """
         }
      }
   }
}
