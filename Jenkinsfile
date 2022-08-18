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
		 sh ''' if [ "${LANG}" != "python" ] && [ "${LANG}" != "all" ];then
		 	 echo "selected value does not match for python"
		 else
			cat *.py
		 fi '''
         }
      }
      stage('c files') {
         steps {
            echo 'c files'
		  sh''' if [ "${LANG}" != "c" ] && [ "${LANG}" != "all" ];then
		 	echo "selected value does not match for c"
		 else
			 cat *.c
		 fi'''
         }
      }
      stage('bash files') {
         steps {
            echo 'bash files'  
		  sh''' if [ "${LANG}" != "bash" ] && [ "${LANG}" != "all" ];then
		 	echo "selected value does not match for bash"
		 else
			 cat *.sh
		 fi'''
         }
      }
      stage('log file') {
         steps {
            echo 'log file'  
		 sh''' cd "${WORKSPACE}/"
		  "commit of ""${LANG}""TIME $(date +%F) ">> logfile
		  '''
         }
      }
      
   }
}
