pipeline {
    agent any

    stages {
        stage('Verify Branch') {
            steps {
                echo "$GIT_BRANCH"
            }
        }
        stage('pwsh Hello'){
            steps {
                pwsh(script 'Write-Out "Hello World"')
            }
        }
        stage('Docker Build') {
            steps {
                pwsh('docker images -a')
            }
        }
    }
}