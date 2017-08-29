pipeline {
  agent {
    docker {
      image 'maven:3-alpine'
      args '-v $HOME/.m2:/root/.m2'
    }
    
  }
  stages {
    stage('build') {
      steps {
        sh 'make'
      }
    }
    stage('Test') {
      steps {
        parallel(
          "Test": {
            sh 'junit \'build/reports/**/*.xml\''
            
          },
          "hello 2": {
            sh 'echo hello'
            
          },
          "hello 3": {
            echo 'test'
            
          }
        )
      }
    }
  }
}