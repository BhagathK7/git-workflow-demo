pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                git 'https://github.com/BhagathK7/git-workflow-demo.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t git-workflow-app .'
            }
        }
    }
}