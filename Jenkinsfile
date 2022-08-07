pipeline {
  agent any
   stages {
      stage('Clone Sources') {
        steps {
          checkout scm
        } 
      }
      stage('python files') {
         steps {
            echo 'python files'
		 echo "${LANG}"
         }
      }
      stage('c files') {
         steps {
            echo 'c files'
         }
      }
      stage('bash files') {
         steps {
            echo 'bash files'    
         }
      }
      
   }
}
