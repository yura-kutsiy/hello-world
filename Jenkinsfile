pipeline {
  agent { label "master" }
  stages {
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
