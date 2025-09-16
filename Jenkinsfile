pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/iamyasodapuli/all-setups.git', branch: 'master'
            }
        }
        stage('Deploy') {
            steps {
                // Example: use docker-compose or kubectl to deploy
                sh "docker-compose -f compose.yml up -d"
            }
        }
    }
}
