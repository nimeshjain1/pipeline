pipeline {
/*	#agent {
	#     label 'slave1'
	#}
*/
	agent any
	stages {
		stage ("checkout")
		{
			steps{
				echo "step 1 checkout";
				checkout scm			

				}
		}
		stage ("build_image")
		{
		    steps{
				echo "step 2 baking image";
				sh 'docker build -t mycluster.icp:8500/testnimesh/myapp docker/' 
				sh 'docker push mycluster.icp:8500/testnimesh/myapp'
				// add the image to the repository in icp. 

			}
		}
/*		stage ("build_helmchart")
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
*/

	}
}
