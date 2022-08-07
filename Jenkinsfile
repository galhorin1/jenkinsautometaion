pipeline {
   agent any

   stages {
      stage('Build') { 
	    steps { 
	    	sh 'echo "My first pipeline"' 
	    	sh ''' 
	    		echo "By the way, I can do more stuff in here" 
	    		ls -la ~ 
	    	''' 
	    } 
}  
      
	  stage('Test') {
         steps {
            echo 'The Test is started'
         }
      }
	  stage('Deploy') {
         steps {
            echo 'The Deploy is started'
         }
      }
      stage('Timeout') { 
	      steps { 
	      	  retry(3) { 
	      	  	  sh 'echo "I am not going to work :c"' 
	      	  }
	      }
      }
      stage('Timeout3') {
	      steps {
	      	  retry(3) { 
	      	  	  sh 'echo hello'
	      	  }
	      	  timeout(time: 3, unit: 'SECONDS') { 
	      	  	  sh 'sleep 5' 
	      	  } 
	      }
      }
   }
}
