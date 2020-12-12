pipeline {
    agent {
        docker { image 'node' }
    }
    stages {
        stage('Build App') {
            steps {
                sh 'npm install -g npm@latest'
                sh 'npm install -g @angular/cli'
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