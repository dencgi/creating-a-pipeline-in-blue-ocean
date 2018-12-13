pipeline {
  agent {
    docker {
      image 'node:6-alpine'
      args '-p 3000:3000'
    }

  }
  stages {
    stage('Test') {
      steps {
        load 'test.groovy'
      }
    }
    stage('Param') {
      steps {
        load 'param.groovy'
	param.toto()
      }
    }
  }
}
