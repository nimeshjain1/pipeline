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
	stages {
		stage ("build")
		{
			steps{
				echo "building 1 anncncncn";
				sh 'docker version'
				sh 'pwd'
				sh 'ls'
				/*dir('jenkins@/home/cloud_user') {
					//sh 'docker build -t mycont .'
					sh 'pwd'
				}*/
				sh 'echo $PATH'
				sh 'which docker'
				sh 'echo $PWD'
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
