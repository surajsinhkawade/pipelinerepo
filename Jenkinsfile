pipeline {
      agent { 
        docker { image 'centos' }
      }
      
      stages {
          stage('Test') {
              steps {
                  sh 'df -kh'
                  sh 'docker ps -a'
              }
          }
      }
}
