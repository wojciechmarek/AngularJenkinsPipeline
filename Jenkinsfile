pipeline {
    agent {
        docker { image 'node:14-alpine' }
    }
    stages {
        stage('Build App') {
            steps {
                sh 'ng build --prod'
            }
        }

        stage('Build Container') {
            steps {
                sh 'docker build -t av-app-image .'
            }
        }
    }
}