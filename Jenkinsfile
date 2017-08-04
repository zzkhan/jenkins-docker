pipeline {
    agent any
    stages {
        stage('build image') {
            steps {
                script{
                    docker.withTool('default') {
                        app = docker.build("mip/test-image", "-f docker-files/test/Dockerfile docker-files/test/")
                    }
                }
            }
        }
        stage('Push image') {
                script {
                    /* Finally, we'll push the image with two tags:
                     * First, the incremental build number from Jenkins
                     * Second, the 'latest' tag.
                     * Pushing multiple tags is cheap, as all the layers are reused. */
                    docker.withRegistry('http://172.17.0.3:5000') {
                        app.push("latest")
                    }
                }
            }
    }
}
