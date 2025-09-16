pipeline {
    agent any
    stages {
        stage('Build & Push Images') {
            steps {
                script {
                    def services = ['db','auth', 'book', 'borrow']
                    for (svc in services) {
                        dir(svc) {
                            sh "docker build -t image/${svc}:latest ./${svc}"
                  
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
