pipeline {
    agent any
    stages {
        stage('build image') {
            steps {
                script{
                    docker.withTool('default') {
                        docker.build("mip/test-image", "-f docker-files/test/Dockerfile docker-files/test/")
                    }
                }
            }
        }
    }
}
