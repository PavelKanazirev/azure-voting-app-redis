pipeline {
    agent any

    stages {
        stage('Verify Branch') {
            steps {
                echo "$GIT_BRANCH"
            }
        }
        stage('GitVer') {
            steps {
                bat 'call git --version'
            }
        }
        stage('Build'){
            steps {                
                powershell 'pwsh --version'
            }
        }        
    }
}