pipeline {
  agent {
    docker {
      image 'node:6-alpine'
      args '-p 3000:3000'
    }

  }
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            sh 'echo build'
          }
        }
        stage('') {
          steps {
            echo 'parallel'
          }
        }
      }
    }
    stage('Test') {
      steps {
        load 'test.groovy'
      }
    }
  }
}