pipeline {
  agent any
  stages {
    stage('Before') {
      steps {
        echo 'before'
      }
    }
    stage('Matrix') {
      parallel {
        stage ('chrome,en-US') {
          steps {
            echo 'chrome,en-US'
          }
        }          
        stage ('chrome,fr-FR') {
          steps {
            echo 'chrome,fr-FR'
          }
        }          
        stage ('firefox,en-US') {
          steps {
            echo 'firefox,en-US'
          }
        }          
        stage ('firefox,fr-FR') {
          steps {
            echo 'firefox,fr-FR'
          }
        }          
        
      }
    }
    stage('After ') {
      steps {
        echo 'after'
      }
    }
  }
}
