pipeline {
  agent {
    dockerfile {
      filename 'DotNetDockerfile'
    }

  }
  stages {
    stage('BuildAndTest') {
      steps {
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