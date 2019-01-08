pipeline {
/*	#agent {
	#     label 'slave1'
	#}
*/
	environment {
		registry = 'mycluster.icp:8500/testnimesh'
		registryCredential='icpcredentials'
		dockerImage = ''
	}
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
				script {	
				docker.build registry+":$BUILD_NUMBER"
				}
				//sh 'docker build -t mycluster.icp:8500/testnimesh/myapp docker/' 
				//sh 'docker login https://mycluster.icp:8500/ -u admin -p admin'
				//sh 'docker push mycluster.icp:8500/testnimesh/myapp'
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
