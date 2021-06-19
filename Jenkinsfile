pipeline{
	agent any
    stages{
        stage("Start Grid"){
            steps{
                bat "docker compose up -d hub chrome firefox"                
            }
        }
        stage("Run tests"){
            steps{
                bat "docker compose up search-module book-flight-module"
            }
        }
        stage("Bring Grid down"){
            steps{
                bat "docker compose down"
            }
        }
    }    
}
