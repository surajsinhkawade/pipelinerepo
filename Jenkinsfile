node {
    checkout scm
    
    def customImage = docker.build("my-image:${env.BUILD_ID}")
    
    customImage.inside {
        sh 'hostname'
        sh 'df -kh'
    }
    
    customImage.push()
    customImage.push('latest')
}
