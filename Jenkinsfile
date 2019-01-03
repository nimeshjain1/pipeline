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
				sh 'docker build -t myapp docker/' 

			}
		}
		stage ("build_helmchart")
		{
		steps{
			dir('helm') {
				echo "deploying"
				sh 'helm init --client-only'
				sh 'helm lint test'
				sh 'helm package test'
			}	
		 }
		}
	}
}
