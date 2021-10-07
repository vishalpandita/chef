pipeline {
  agent any
  stages {
    stage('step') {
      agent {
        node {
          label 'slave'
        }

      }
      steps {
        sh 'docker pull hello-world'
        sh 'docker tag hello-world vishalpandita/hello-world'
        sh 'docker push vishalpandita/hello-world'
      }
    }

  }
}