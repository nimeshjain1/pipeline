pipeline {
    agent any
    stages {
        stage ("build")
        {
            steps{
                echo "building 1 anncncncn"
		cd docker
                docker build -t myweb .
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
