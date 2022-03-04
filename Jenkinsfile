pipeline {
    agent any

    stages {
        stage('Verify Branch') {
            steps {
                echo "$GIT_BRANCH"
            }
        }
        stage('Docker Build') {
            steps {
                sh 'git --version'
                dir('azure-vote') {
                    sh 'docker images -a'
                    // some block
                }

                sh 'cd ..'
            }
        }
    }
}