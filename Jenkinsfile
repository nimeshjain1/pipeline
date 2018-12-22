pipeline {
    agent{
      dockerfile {
//	args '-t myweb1'
	dir 'docker'
	filename 'Dockerfile'
      }
    }
    stages {
        stage ("build")
        {
            steps{
                echo "building 1 anncncncn";
		sh 'pwd'
		/*dir('/home/cloud_user/pipeline') {
			sh '/bin/docker build -t mycont .'
		}*/
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
