pipeline {
  agent {
    node {
      label 'master'
    }
    
  }
  stages {
    stage('error') {
      steps {
        input(message: 'Pick your browser', id: 'Browser')
      }
    }
  }
}