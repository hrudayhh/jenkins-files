import groovy.json.*
pipeline {
    agent any
        stages {  
            stage('get code') {
              git credentialsId: 'pl_test', url: 'https://github.com/hrudayhh/pl_test.git'
            }
            stage('convert to json') {
              def data = readYaml file: config.yml
              def json = new JsonBuilder(data).toPrettyString()
              writeFile file: config.json, text: json
            }
        }
}
