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
		 sh ''' if [ "${LANG}" -ne "python" ] && [ "${LANG}" -ne "all" ];then
		 	 echo "selected value does not match for python"
		 else
			cat *.py
		 fi '''
         }
      }
      stage('c files') {
         steps {
            echo 'c files'
		  sh''' if [ "${LANG}" -ne "c" ] && [ "${LANG}" -ne "all" ];then
		 	echo "selected value does not match for c"
		 else
			 cat *.c
		 fi'''
         }
      }
      stage('bash files') {
         steps {
            echo 'bash files'  
		  sh''' if [ "${LANG}" -ne "bash" ] && [ "${LANG}" -ne "all" ];then
		 	echo "selected value does not match for bash"
		 else
			 cat *.sh
		 fi'''
         }
      }
      
   }
}
