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
		stage ("checkout")
		{
			steps{
				echo "building 1 anncncncn";
				checkout scm			

				}
		}
		stage ("build_image")
		{
		    steps{
			echo "testing 2 hello from Nimesh"
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
