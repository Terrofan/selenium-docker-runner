pipeline{
	agent any
    stages{
        stage("Run Test"){
            steps{
                bat "docker compose up -d hub chrome firefox"
                bat "docker compose up search-module book-flight-module"
            }
        }
        stage("Bring down"){
            steps{
                bat "docker compose down"
            }
        }
    }    
}
