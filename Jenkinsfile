pipeline {
    agent {
        kubernetes {
            label "uiui"
            defaultContainer 'jnlp'
            yamlFile 'Pod.yaml'
            }
        }
    stages {
        stage("checkout"){
            steps {
                container('git'){
                    sh "ls -l"
                    }
                
                }

            }
        stage("Maven Build") {
            steps {
                container('maven') {
                   
                       sh "ls -l"
                     
                    }
                }
            }   
    }
    
}
