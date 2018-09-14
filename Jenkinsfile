node {
    checkout scm
    
    def customImage = docker.build("my-image:${env.BUILD_ID}")
    
    customImage.inside {
        sh 'hostname'
        sh 'df -kh'
    }
    
     docker.withRegistry('https://registry.hub.docker.com', 'docker-hub-credentials') {
            customImage.push("${env.BUILD_NUMBER}")
            customImage.push("latest")
        }
    
    //customImage.push()
    //customImage.push('latest')
}
