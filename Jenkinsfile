pipeline {
  agent any
  stages {
    stage('Dev') {
      parallel {
        stage('Dev') {
          steps {
            echo 'Dev Stage'
          }
        }
        stage('dev1') {
          steps {
            sleep 10
          }
        }
      }
    }
    stage('SIT') {
      steps {
        echo 'SIT Stage'
      }
    }
    stage('UAT') {
      steps {
        echo 'UAT Stage'
      }
    }
  }
}