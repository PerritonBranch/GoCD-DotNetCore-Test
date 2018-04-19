pipeline {
  agent {
    docker {
      image 'node:6-alpine'
      args '''-p 3000:3000
'''
    }

  }
  stages {
    stage('TestDockerCommands') {
      steps {
        sh 'cat /etc/*-release'
        sh 'whoami'
        sh '''apk update
apk add docker'''
        sh 'docker ps'
        sh 'docker --version'
        sh 'docker run hello world'
      }
    }
  }
}