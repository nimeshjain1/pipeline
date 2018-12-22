pipeline {
/*    agent{
      dockerfile {
//	args '-t myweb1'
	dir 'docker'
	filename 'Dockerfile'
      }
    }
*/
    agent any
    node {
    	stages {
        	stage ("build")
        	{
            	steps{
                	echo "building 1 anncncncn";
			//sh 'docker build -t myweb .'
			dir('/home/cloud_user/pipeline') {
				//sh 'docker build -t mycont .'
				sh 'pwd'
			}
            	}
       		}
        	stage ("test")
        	{
        	    steps{
                	echo "testing 2 hello from Nimesh"
            		}
        	}
        	stage ("deploy")
        	{
            	steps{
                	echo "deploying"
           	 }
        	}
    	}
   }	
}
