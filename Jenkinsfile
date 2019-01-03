pipeline {
	agent {
	     label 'slave1'
	}
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
				//sh 'docker build -t myapp docker/' 
				echo env.workspace
				//sh 'helm create mytest'	
				sh 'git --version'

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
