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
        BITBUCKET_COMMON_CREDS = credentials('jenkins-bitbucket-common-creds')
    }
            steps {
                
                echo "${BITBUCKET_COMMON_CREDS_USR}"
                echo "${BITBUCKET_COMMON_CREDS_PSW}"
            }
        }
    }
}
