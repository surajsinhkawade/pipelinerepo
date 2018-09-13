pipeline {
    agent any
    stages {
          stage('Build'){
              steps {
                  sh 'Building Software'
              }
          }
        
        stage('ParallelExecute'){
        
            parallel {
            echo ' Running Parallel on Linux'
            },
                 {
            echo ' Running Parallel on Windows'    
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
