pipeline{
    
    agent any
    stages{
        
        // Connect to GitHub
        stage('Create postgresql image'){
            steps{
               sh 'cd apache/postgresql && sudo docker build -t custpostgresql . '
               sh 'sudo docker images'
            }
        }

        stage('Run Docker postgresql Container from image'){
            steps{
               sh 'sudo docker run -dit --name=postgresql01 custpostgresql'
               sh 'sudo docker ps'
               sh 'sudo docker stop postgresql01'
            }
        }
        
    }
}

