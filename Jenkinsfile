import groovy.json.*
    def data = readYaml('config.yml')
    writeFile file: 'config.json', text: '${data}'
    
pipeline {
    agent any
        stages {  
            stage('get code') {
                steps {
                    git credentialsId: 'pl_test', url: 'https://github.com/hrudayhh/pl_test.git'
                }
            }
            stage('convert to json') {
                steps {
                    script {
                        echo 'converted'
                    }
                //def json = new JsonBuilder(data).toPrettyString()        
                }  
            }
        }
}
