pipeline {
    agent any
    environment {
        TERM = "xterm"
         username = 'surajsinh'
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
                
                 echo " Printing user Name: ${username}"
                echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}"
            }
        }
    }
}
