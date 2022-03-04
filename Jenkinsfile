pipeline {
    agent any

    stages {
        stage('Verify Branch') {
            steps {
                echo "$GIT_BRANCH"
            }
        }
        stage('Build'){
            steps {
                powershell 'pwsh --version'
            }
        }        
    }
}