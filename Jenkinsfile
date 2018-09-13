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
                sh 'wget --no-check-certificate --no-cookies --header "Cookie: oraclelicense=accept-securebackup-cookie" http://download.oracle.com/otn-pub/java/jdk/${JAVA_VERSION}-b${JAVA_BUILD}/d54c1d3a095b4ff2b6607d096fa80163/jdk-${JAVA_VERSION}-linux-x64.rpm'
                sh 'mvn --version'
                sh 'ls -ltr /var/lib/jenkins/tools/hudson.model.JDK/jdk/*'
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
