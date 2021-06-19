pipeline{
	agent any
    stages{
        stage("Pull Latest Image"){
            bat "docker pull terrofan/selenium-docker"
        }
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
    }
    post{
        always{
            archiveArtifacts artifacts: 'output/**'
            bat "docker compose down"
        }
    }
}
