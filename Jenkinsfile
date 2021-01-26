import groovy.json.*
    def data = readYaml file: 'config.yml'
    writeFile file: 'config.json', json: data
    
pipeline {
    agent any
        stages {  
            stage('get code') {
                steps {
                    git credentialsId: 'pl_test', url: 'https://github.com/hrudayhh/pl_test.git'
                }
            }
            stage('convert to json') {
                //steps {
                println(data)        
                        //def json = new JsonBuilder(data).toPrettyString()
                        
                //}  
            }
        }
}
