pipeline {
  agent any
   stages {
      stage('Clone Sources') {
        steps {
          checkout scm
        } 
      }
	   stage('all files') {
		   steps{
		   if ( "${LANG}" == "all" );then
			   cat *
			exit 0
		   }
	   }
      stage('python files') {
         steps {
            echo 'python files'
		  if ( "${LANG}" == "python" );then
		 	cat *.py
		 else
			 echo "selected value does not match for python"
		 fi
         }
      }
      stage('c files') {
         steps {
            echo 'c files'
		  if ( "${LANG}" == "c" );then
		 	cat *.c
		 else
			 echo "selected value does not match for c"
		 fi
         }
      }
      stage('bash files') {
         steps {
            echo 'bash files'  
		  if ( "${LANG}" == "bash" );then
		 	cat *.sh
		 else
			 echo "selected value does not match for bash"
		 fi
         }
      }
      
   }
}
