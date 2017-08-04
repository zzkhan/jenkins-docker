pipeline {
    agent any
    tools {
        docker 'docker'
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
