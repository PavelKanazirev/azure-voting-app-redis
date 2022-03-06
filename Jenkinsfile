@Library('github.com/PavelKanazirev/demo-shared-pipeline') _

pipeline {
    agent any

    stages {
        stage('Call Library Function') {
            steps {
                script {
                    helloArgs('Jenkins!')
                }
            }
        }
        stage('Call Additional Library Function') {
            steps {
                script {
                    helloArgs.goodbyeWorld('Jenkins!')
                }
            }
        }
    }
}