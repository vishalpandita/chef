pipeline {
  agent {
    docker {
      image 'maven:3.8.1-adoptopenjdk-11'
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