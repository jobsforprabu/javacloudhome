pipeline {
    agent any
    environment{
        DOCKER_TAG=getDockerTag()
    }
    stages {
        stage('Build Docker Image') {
            steps{
                sh "docker build -t  prganesh/nodeapp:v1"
            }

        }
    }
}

#utility method to define the docker tag

def getDockerTag(){
    def tag = sh script: 'git rev-parse HEAD', returnStdout: true
    return tag
}