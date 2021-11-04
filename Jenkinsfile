pipeline {
   agent any

    stages {
      stage('Verify Branch') {
         steps {
            echo "$GIT_BRANCH"
<<<<<<< HEAD
         }
      }
      stage('Docker Build') {
         steps {
            sh 'pwd'
            sh 'docker images -a'
            // sh """ 
            //    cd azure-vote/
            //    docker images -a .
            //    docker build -t jenkins-pipeline .
            //    docker images -a
            //    cd ...
            // """
=======
            sh 'echo "hello"'
>>>>>>> b8a6ea96306ea2cbe28f0d191442ffdd050f2024
         }
      }
   }
}
