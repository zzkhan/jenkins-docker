pipeline {
    agent any
    tools {
        org.jenkinsci.plugins.docker.commons.tools.DockerTool 'docker'
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
