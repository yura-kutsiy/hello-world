pipeline {
  agent { label "master" }
  stages {
    stage('Initialize'){
        def dockerHome = tool '1docker'
        env.PATH = "${dockerHome}/bin:${env.PATH}"
    }
    stage("build") {
      steps {
        sh """
          docker build -t hello-world .
        """
      }
    }
    stage("run") {
      steps {
        sh """
          docker run --rm hello-world
        """
      }
    }
  }
}
