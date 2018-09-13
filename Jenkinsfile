pipeline {
    agent any
    environment {
        TERM = "xterm"
        }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            when {
              expression {
                currentBuild.result == null || currentBuild.result == 'SUCCESS' 
              }
            }
            
            
            steps {         
                 //sh 'top'
                
                  sh 'df -kh'
                
                 def username = 'surajsinh'
                echo " Printing user Name: ${username}"
            }
        }
    }
}
