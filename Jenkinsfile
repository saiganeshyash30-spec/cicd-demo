pipeline {
    agent any
    stages {
        stage('Clone Code') {
            steps {
                git branch: 'main', url: 'https://github.com/saiganeshyash30-spec/cicd-demo.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t cicd-demo-image .'
            }
        }
        stage('Run Container') {
            steps {
                sh 'docker run -d -p 8081:80 cicd-demo-image'
            }
        }
    }
}
