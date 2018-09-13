pipeline {
    agent none
    stages {
        stage('Back-end') {
            agent {
                docker { image 'maven:3-alpine' }
            }
            environment {
                JAVA_HOME = "/var/lib/jenkins/tools/hudson.model.JDK/jdk/"
            }
            steps {
                echo "$JAVA_HOME"
                sh 'mvn --version'
            }
        }
        stage('Front-end') {
            agent {
                docker { image 'node:7-alpine' }
            }
            steps {
                sh 'node --version'
            }
        }
    }
}
