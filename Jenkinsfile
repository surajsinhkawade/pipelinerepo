pipeline {
  agent {
    docker {
      image 'centos'
    }

  }
  stages {
    stage('dev') {
      steps {
        sh 'df -kh'
      }
    }
  }
  environment {
    TERM = 'xterm'
  }
}