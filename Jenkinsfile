pipeline {
  agent any
  stages {
    stage('Before') {
      steps {
        echo 'before'
      }
    }
    stage('Matrix') {
      steps {
        echo 'Hello World'
        script {
          def browsers = ['chrome', 'firefox']
          for (int i = 0; i < browsers.size(); ++i) {
            echo "Testing the ${browsers[i]} browser"
          }
          
          def axisBrowser = ["chrome","firefox"]
          def axisLanguage = ["en-US","fr-FR"]
          def tasks = [:]
          for(int i=0; i< axisBrowser.size(); i++) {
            def axisBrowserValue = axisBrowser[i]
            for(int j=0; j< axisLanguage.size(); j++) {
              def axisLanguageValue = axisLanguage[j]
              tasks["${axisBrowserValue}/${axisLanguageValue}"] = {
                steps {
                  println "Browser=${axisBrowserValue}"
                  println "Language=${axisLanguageValue}"
                }
              }
            }
          }
          parallel tasks
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