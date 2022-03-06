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
            when { branch 'add-tests'}
            steps {
                echo "Workspace is $WORKSPACE"
                echo 'This is the add-tests branch'
            }
        }
    }
}