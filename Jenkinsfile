pipeline {
    agent {
        docker {
            image 'node:14-alpine'
            args '-v $HOME:/home/jenkins'
        }
    }

    stages {
        stage('Verify Branch') {
            steps {
                echo "$GIT_BRANCH"
            }
        }
        stage('Docker Build') {
            steps {
                sh 'docker images -a'
            }
        }
    }
}