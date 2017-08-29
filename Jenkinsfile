pipeline {
  agent {
    docker {
      image 'test'
      args 'test'
    }
    
  }
  stages {
    stage('hello') {
      steps {
        echo 'hello'
      }
    }
  }
}