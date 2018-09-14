node {
    checkout scm
    
    //def customImage = docker.build("my-image:${env.BUILD_ID}")
    docker.withRegistry('https://registry.hub.docker.com/surajsinhkawade/my-image/', 'docker-hub-credentials') {
        def customImage = docker.build("my-image:${env.BUILD_ID}")
             
        customImage.inside {
        sh 'hostname'
        sh 'df -kh'
         }
    
     //docker.withRegistry('https://registry.hub.docker.com', 'docker-hub-credentials') {
    //docker.withRegistry('https://hub.docker.com/r/surajsinhkawade/demorep/', 'docker-hub-credentials') {
    //docker.withRegistry('https://hub.docker.comr/surajsinhkawade', 'docker-hub-credentials') {
            customImage.push("${env.BUILD_NUMBER}")
            customImage.push("latest")
        }
    
    //customImage.push()
    //customImage.push('latest')
}
