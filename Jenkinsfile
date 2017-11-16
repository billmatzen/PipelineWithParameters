pipeline {

  def axisBrowser = ["chrome","firefox"]
  def axisLanguage = ["en-US","fr-FR"]
  def tasks = [:]
    
  agent {
    node {
      label 'master'
    }

  }
  stages {

    stage("Before") {
        node {
            echo "before"
        }
    }

    for(int i=0; i< axisBrowser.size(); i++) {
        def axisBrowserValue = axisBrowser[i]
        for(int j=0; j< axisLanguage.size(); j++) {
            def axisLanguageValue = axisLanguage[j]
            tasks["${axisBrowserValue}/${axisLanguageValue}"] = {
                    println "Browser=${axisBrowserValue}"
                    println "Language=${axisLanguageValue}"
            }
        }
    }

    stage ("Matrix") {
        parallel tasks
    }

    stage("After ") {
        node {
            echo "after"
            
        }
    }
  }
}
