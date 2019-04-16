pipeline {
    agent {
        kubernetes {
            label "uiui"
            defaultContainer 'jnlp'
            yaml 
            }
        }
    stages {
        stage("checkout"){
            steps {
                container('git'){
                  git credentialsId: 'artifactorygdn', url: 'https://github.com/m2c-team/docker_build_script.git', branch: 'master'    
                    sh "ls -l"
                    }
                
                }

            }
        stage("Maven Build") {
            steps {
                container('maven') {
                    withCredentials([file(credentialsId: "artifactorygdn", variable: 'SA')]) {
                       sh("mvn clean install")
                        }
                    }
                }
            }   
    }
    
}
