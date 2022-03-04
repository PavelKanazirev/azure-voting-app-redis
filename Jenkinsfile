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
                pwsh(script: 'docker images -a')
            }
        }
        stage('Docker PS') {
            steps {
                pwsh(script: 'docker ps -a')
            }
        }
    }
}