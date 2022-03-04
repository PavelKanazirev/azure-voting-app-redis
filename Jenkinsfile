pipeline {
    agent any

    stages {
        stage('Verify Branch') {
            steps {
                echo "$GIT_BRANCH"
            }
        }
        stage('pwsh doc'){
            steps {
                pwsh 'docker images -a'
            }
        }        
    }
}