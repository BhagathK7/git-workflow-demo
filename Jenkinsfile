pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                git 'https://github.com/your-username/git-workflow-demo.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t git-workflow-app .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 5000:5000 git-workflow-app'
            }
        }
    }
}