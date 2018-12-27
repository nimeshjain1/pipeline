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
				checkout scm			

				}
		}
		stage ("test")
		{
		    steps{
			echo "testing 2 hello from Nimesh"
				sh 'docker version'
				sh 'pwd'
				sh 'ls'
				sh 'which docker'
				sh 'docker build -t myapp docker/' 
				sh 'echo $PWD'

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
