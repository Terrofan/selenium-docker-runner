pipeline{
	agent any
    stages{
        stage("Run Test"){
            steps{
                bat "docker compose up"
            }
        }
        stage("Bring down"){
            steps{
                bat "docker compose down"
            }
        }
    }    
}
