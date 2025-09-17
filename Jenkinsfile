pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/iamyasodapuli/python-code-library-app.git', branch: 'master'
            }
        }
        stage('Deploy') {
            steps {
                // Example: use docker-compose or kubectl to deploy
                sh "docker-compose up -d"
            }
        }
    }
}
