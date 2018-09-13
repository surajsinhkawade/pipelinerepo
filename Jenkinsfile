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
         environment {
         
         username = 'kawade'
        }
            
            steps {         
                 //sh 'top'
                
                  sh 'df -kh'
                
                 echo " Printing user Name: ${username}"
                echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}"
            }
        }
        
        stage('ManageCredentials'){
                environment {
        AWS_ACCESS_KEY_ID = credentials('jenkins-aws-secret-key-id')
        AWS_SECRET_ACCESS_KEY = credentials('jenkins-aws-secret-access-key')
    }
            steps {
                
                echo "${AWS_ACCESS_KEY_ID}"
                echo "${AWS_SECRET_ACCESS_KEY}"
            }
        }
    }
}
