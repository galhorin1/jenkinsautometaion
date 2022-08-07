pipeline {
   agent any
  
   stages {
      	stage('build') {
         steps {
            sh echo 'this is the build step here we down load the files to our local machine'
         }
      }
      	stage('python') {
         steps {
           sh echo 'this is the python file step'
         }
      }
	  stage('c') {
         steps {
           sh echo 'this is the c file step'
         }
      }
	  stage('bash') {
         steps {
          sh echo 'this is the bash file step'
         }
      }
   }
}
