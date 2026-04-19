pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                git branch: 'dev', url: 'https://github.com/BhagathK7/git-workflow-demo.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t git-workflow-app .'
            }
        }

        stage('Stop Old Container') {
            steps {
                sh 'docker stop git-container || true'
                sh 'docker rm git-container || true'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 5000:5000 --name git-container git-workflow-app'
            }
        }
    }
}