pipeline
{
   agent none
    
    triggers { cron('H */4 * * 1-5') }
    
 parameters { choice(name: 'CHOICES', choices: ['one', 'two', 'three'], description: '') }
    
    stages{
        
        stage("build"){
        
         agent {
    docker 
        {
        image 'maven'
        }
    } 
            steps{
                sh 'mvn -version'
            }
            
        }
        stage("test"){
        
         agent {
    docker 
        {
        image 'gradle'
        }
    } 
            steps{
                sh 'gradle --version'
            }
            
        }
    }
    
    
    
}
