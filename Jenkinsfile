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
        echo 'hello buddy'
        sh 'hostname'
      }
    }
  }
  environment {
    TERM = 'xterm'
  }
}