pipeline {
  agent any
  stages {
    stage('BuildAndTest') {
      steps {
        sh 'docker --version'
        sh 'whoami'
        sh 'groups jenkins'
        sh 'docker run hello-world'
        sh 'cat /etc/*-release'
        sh 'dotnet restore Builder.sln'
        sh 'dotnet build Builder.sln'
        sh 'dotnet test Builder.sln'
      }
    }
    stage('DockerBuild') {
      steps {
        sh 'docker run hello-world'
      }
    }
  }
}