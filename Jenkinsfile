pipeline{
    
    agent any
    stages{
        
        // Connect to GitHub
        stage('Create postgresql image'){
            steps{
               sh 'cd apache/postgresql && sudo docker build -t custpostgredql . '
               sh 'sudo docker images'
            }
        }
        
    }
}

