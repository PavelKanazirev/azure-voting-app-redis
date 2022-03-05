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
                    script {
                        docker.withRegistry('https://index.docker.io/v1/','DockerHub'){
                            def image = docker.build('pavelkanazirev/docker101tutorial:latest')
                            image.push()
                        }
                    }
                }
            }
        }
    }
}