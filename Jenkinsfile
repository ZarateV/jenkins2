import groovy.json.JsonSlurperClassic

def jsonParse(def json){
    new groovy.json.jsonParseClassic().parseText(json)
}
pipeline {
    agent {label 'master' }
    environment {
        appName = "variable"
    }
    stages{

        stage("paso 1"){

            steps{
                script{
                    sh "echo 'Hola muno'"
                }
            }
        }
    }
    post {
        always {
            deleteDir()
            sh "echo 'fase always'"
        }
        success {
            sh "echo 'fase success'"
        }
        failure {
            sh "echo 'fase failure'"
        }
    }
}