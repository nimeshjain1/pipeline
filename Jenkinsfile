pipeline {
    agent any
    stages {
        stage ("build")
        {
            steps{
                echo "building 1 anncncncn";
		sh 'pwd'
		//sh '/bin/docker build -t mycont .'
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
