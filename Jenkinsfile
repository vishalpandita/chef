pipeline {
  agent {
    docker {
      image 'vishalpandita/maven:3.8.1-adoptopenjdk-11-docker'
      args '-v /home/.m2:/root/.m2 -e HTTP_PROXY="http://209.58.84.119:3128" -e HTTPS_PROXY="http://209.58.84.119:3128" --dns 8.8.8.8 --env DOCKER_HOST=tcp://10.10.154.34:2376 '
    }

  }
  stages {
    stage('step') {
      steps {
        sh 'docker pull hello-world'
        sh 'docker tag hello-world vishalpandita/hello-world'
        sh 'docker push vishalpandita/hello-world'
      }
    }

  }
}