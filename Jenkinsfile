pipeline {
    agent any

    stages {
        stage('Build & Push Docker Image') {
            steps {
                script {
                    withDockerRegistry([credentialsId: 'docker-cred', url: 'https://index.docker.io/v1/']) {

                        dir('src') {
                            sh "docker build -t adijaiswal/checkoutservice:latest ."
                        }

                        sh "docker push adijaiswal/checkoutservice:latest"
                    }
                }
            }
        }
    }
}
