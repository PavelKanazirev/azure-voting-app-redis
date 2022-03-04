pipeline {
    agent any

    stages {
        stage('Win') {
            steps {
                powershell 'Write-Output "Hello, World!"'
            }
        }
        stage('Verify Branch') {
            steps {
                echo "$GIT_BRANCH"
            }
        }       
    }
}