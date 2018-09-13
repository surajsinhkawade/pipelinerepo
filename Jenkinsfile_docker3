pipeline {
    agent {
        docker {
            image 'maven:3-alpine'
            args '-v $HOME/.m2:/root/.m2'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'which java'
                sh 'java -version'
                sh 'mkdir -p /opt/java'
                sh 'cd /opt/java'
                
                sh 'mvn -B'
            }
        }
    }
}
