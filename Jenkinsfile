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
		   sh ''' if [ "${LANG}" == "all" ];then
			   cat *
			exit 0
			fi'''
		   }
	   }
      stage('python files') {
         steps {
            echo 'python files'
		 sh ''' if [ "${LANG}" == "python" ];then
		 	cat *.py
		 else
			 echo "selected value does not match for python"
		 fi '''
         }
      }
      stage('c files') {
         steps {
            echo 'c files'
		  sh''' if [ "${LANG}" == "c" ];then
		 	cat *.c
		 else
			 echo "selected value does not match for c"
		 fi'''
         }
      }
      stage('bash files') {
         steps {
            echo 'bash files'  
		  sh''' if [ "${LANG}" == "bash" ];then
		 	cat *.sh
		 else
			 echo "selected value does not match for bash"
		 fi'''
         }
      }
      
   }
}
