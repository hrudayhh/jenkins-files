pipeline {
    agent any
        stages {  
            stage('build') {
                steps {
                    script {
                        try {
                            sh "mvn clean install"
                        } 
                        catch (Exception err) {
                            echo 'Maven clean install failed'
                            currentBuild.result = 'FAILURE'
                        } 
                        finally {
                            publishHTMLReports('Reports')
                        }
                    }
                }
            }
        }
}
