pipeline {
	#agent {
	#     label 'slave1'
	#}
	
	stages {
		stage ("checkout")
		{
			steps{
				echo "building 1 checkout";
				checkout scm			

				}
		}
		stage ("build_image")
		{
		    steps{
				echo "building 1 baking image";
				sh 'docker build -t myapp docker/' 
				// add the image to the repository in icp. 

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
				archiveArtifacts 'test-0.1.0.tgz'
			}	
		 }
		}
	}
}
