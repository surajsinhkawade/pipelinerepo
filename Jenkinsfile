pipeline {
      agent { 
        docker { image : 'node:centos' }
      }
      
      stages {
          stage('Test') {
              steps {
                  sh 'node --version'
              }
          }
      }
}
