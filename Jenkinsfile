pipeline {
    agent {
        minikube {
            label "uiui"
            defaultContainer 'jnlp'
            yamlFile 'Pod.yaml'
            }
        }
    node('uiui') {
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
