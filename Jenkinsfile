pipeline{
    
    agent any
    stages{
        
        // Connect to GitHub
        stage('Connect to Github create image'){
            steps{
               sh 'rm -Rf 730am'
               sh 'git clone https://github.com/SUSIGUGH/730am.git'
               sh 'cd 730am/docker && sudo docker build -t httpdimg . '
               sh 'sudo docker run -dit --name=httpd01 httpdimg'
            }
        }
        
    }
}

