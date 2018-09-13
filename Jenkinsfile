pipeline {
      agent { 
        docker { image 'centos' }
      }
      
      stages {
          stage('Test') {
              steps {
                  sh 'df -kh'
                  sh 'yum install httpd'
              }
          }
      }
}
