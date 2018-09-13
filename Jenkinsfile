pipeline {
    agent any
    stages {
          stage('Build'){
              steps {
                  echo 'Building Software'
              }
          }
        
        stage('ParallelExecute'){
            steps {
            parallel( 
                a: {
            echo ' Running Parallel on Linux'
            },
                b: {
            echo ' Running Parallel on Windows'    
            }
           )
          }
        }
    }
    
    post {
        always {
        
            echo 'Always Success'
        }
        
        unstable{
            echo 'Unstable Build'
        
        }
        
        success{
            echo ' Successful Mail'
        }
        
        failure{
            echo 'Failure mail'
        }
        
        changed{
            echo 'Stage Changed'
        }
        
    }
}
