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
            }
        }
        stage('Start test app') {
            steps {
                sh 'git --version'
            }
            post {
                success {
                    echo "App started successfully"
                }
                failure {
                    echo "App failed to start"
                }
            }
        }
        stage('Push Container') {
            steps {
                echo "Workspace is $WORKSPACE"
                dir("$WORKSPACE/azure-vote"){
                    sh 'ls'
                }
            }
        }
    }
}