pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/iamyasodapuli/python-code-library-app.git', branch: 'master'
            }
        }

        stage('Build & Push Images') {
            steps {
                script {
                    def services = ['db','auth', 'book', 'borrow']
                    for (svc in services) {
                        dir(svc) {
                            sh "docker build -t your-dockerhub/${svc}:latest ./${svc}"
                  
                        }
                    }
                }
            }
        }

        stage('Deploy') {
            steps {
                // Example: use docker-compose or kubectl to deploy
                sh "docker-compose -f docker-compose.yml up -d"
            }
        }
    }
}
