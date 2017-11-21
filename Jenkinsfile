pipeline {

  agent any 
    
    stages {
  
     
    
    stage("Before") {
        steps {
            echo "before"
        }
    }

    stage ("Matrix") {
        steps {
 
          echo 'Hello World'
          
          script {
              def browsers = ['chrome', 'firefox']
              for (int i = 0; i < browsers.size(); ++i) {
                  echo "Testing the ${browsers[i]} browser"
              }
          }
        }
    }

    stage("After ") {
        steps {
            echo "after"
            
        }
    }
  }
}
