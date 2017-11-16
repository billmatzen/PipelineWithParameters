pipeline {

    def axisBrowser = ["chrome","firefox"]
    def axisLanguage = ["en-US","fr-FR"]
    def tasks = [:]

    stage("Before") {
        node {
            echo "before"
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
