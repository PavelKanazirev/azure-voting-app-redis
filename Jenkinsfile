@Library('github.com/PavelKanazirev/demo-shared-pipeline') _

pipeline {
    agent any

    stages {
        stage('Call Library Hello-World Function') {
            steps {
                script {
                    helloArgs('Jenkins!')
                }
            }
        }
        stage('Call Library Hello-World Function') {
            steps {
                script {
                    helloArgs.goodbyeWorld('Jenkins!')
                }
            }
        }
    }
}