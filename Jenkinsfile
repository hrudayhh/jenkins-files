import groovy.json.*
    
    //writeFile file: 'config.json', text: '${data}'
    
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
                        def data = readYaml file: 'config.yml'
                        println(data)
                    }
                //def json = new JsonBuilder(data).toPrettyString()        
                }  
            }
        }
}
