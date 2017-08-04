pipeline {
    agent any
    tools {
        Docker 'docker'
    }
    stages {
        stage('build image') {
            steps {
                script{
                    app = docker.build("mip/test-image")    
                }
            }
        }
    }
}
