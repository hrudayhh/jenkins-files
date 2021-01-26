import groovy.json.*
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
                        def data = readYaml file: 'config.yml'
                        //def json = new JsonBuilder(data).toPrettyString()
                        writeJson file: 'config.json', json: data
                //}  
            }
        }
}
