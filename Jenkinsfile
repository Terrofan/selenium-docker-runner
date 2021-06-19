pipeline{
	agent any
    stages{
        stage("Run Test"){
            steps{
                bat "docker compose up"
            }
        }
        stage("Run Test"){
            steps{
                bat "docker compose down"
            }
        }
    }    
}
