pipeline {
    agent any
    
    stages{
        
             stage('Dev'){
                 steps{
                
                        echo 'Hello World'
                
                
                        emailext attachLog: true, body: 'Please check the new build from jenkins', compressLog: true, recipientProviders: [developers()], subject: 'Please check the new build', to: 'surajsinh.kawade@oracle.com'
                
                        fileExists 'test.txt'
                            echo 'True'
                     
                        }
            
            
                }
        
        stage('Confirm'){
            steps{
                input message: 'Confirmation4NextStep', ok: 'Confirm'
            }
        }
        
            stage('VerifyFiles'){
                steps {
                    
                    pwd()
                    fileExists 'test.txt'
                    fileExists 'abcd.txt'
                            echo 'True'
                     
                       }
                }
        
        stage('DisplayEnv'){
            steps {
            echo 'env.BRANCH_NAME'
                echo '{env.BUILD_NUMBER}'
            echo 'env.BUILD_ID'
                {JOB_NAME}
                {env.JENKINS_HOME}
            }
        }
        
    }
    
}
