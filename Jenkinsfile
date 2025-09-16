pipeline {
    agent any
    stages {
        stage('Deploy') {
            steps {
                // Example: use docker-compose or kubectl to deploy
                sh "docker-compose -f compose.yml up -d"
            }
        }
    }
}
