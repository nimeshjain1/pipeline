pipeline {
/*	#agent {
	#     label 'slave1'
	#}
*/
	environment {
		registry = 'mycluster.icp:8500/testnimesh'
		registryCredential='icpcredentials'
		dockerImage = '/myapp'
		customImage = ''
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
				docker.withRegistry('http://mycluster.icp:8500',registryCredential) {
					def image = docker.build(registry+dockerImage+":$BUILD_NUMBER", 'docker')
					image.push("latest")
				}
				} 
				

			}
		}
		stage ("build_helmchart")
		{
		steps{

			dir('helm') {
				echo "deploying"
				sh 'helm init --client-only'
				sh 'helm lint test'
				sh 'helm package rrdemo'
				archiveArtifacts 'rrdemo-0.1.1.tgz'
				//sh 'bx pr --help'
				sh 'bx pr login -u admin -p admin -a https://192.168.2.2:8443/ --skip-ssl-validation -c id-mycluster-account'
				sh 'bx pr target -n testnimesh'
				sh 'bx pr load-helm-chart --archive rrdemo-0.1.1.tgz'
			}	

		 }
		}


	}
}
