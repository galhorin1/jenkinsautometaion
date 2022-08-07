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
		 script {
			 if (${LANGUAGE} == 'all')||(${LANGUAGE}  == 'python') ) {
                        sh cat *.py
                    } else {
                        echo 'selected field does not match python/all'
                    }
                }
         }
      }
      stage('c files') {
         steps {
            echo 'c files'
		  script {
                    if ((${LANGUAGE} == 'all')||(${LANGUAGE} == 'c') ) {
                        sh cat *.c
                    } else {
                        echo 'selected field does not match c/all'
                    }
                }
         }
      }
      stage('bash files') {
         steps {
            echo 'bash files'    
		  script {
                    if ((${LANGUAGE} == 'all')||(${LANGUAGE} == 'bash') ) {
                        sh cat *.sh
                    } else {
                        echo 'selected field does not match shell/all'
                    }
                }
         }
      }
      
   }
}
