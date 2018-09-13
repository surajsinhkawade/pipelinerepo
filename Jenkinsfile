pipeline {
    agent any
    
    stages{
        
        stage('Dev'){
            steps{
                
                echo 'Hello World'
                
                /*dir('BuildDir/') {
                    sh 'pwd'
                }*/
                
                emailext attachLog: true, body: 'Please check the new build from jenkins', compressLog: true, recipientProviders: [developers()], subject: 'Please check the new build', to: 'surajsinh.kawade@oracle.com'
                
                fileExists 'test.txt'
                
            }
            
            
        }
        
        stage('VerifyFiles'){
            steps {
            fileExists 'test.txt'
            fileExists 'abcd.txt'
            }
    }
}
