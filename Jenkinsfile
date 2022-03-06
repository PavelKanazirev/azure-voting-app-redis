@Library('https://github.com/PavelKanazirev/demo-shared-pipeline')

pipeline {
    agent any

    stages {
        stage('Call Library Hello-World Function') {
            steps {
                script {
                    helloWorld()
                }
            }
        }
 
    }
}