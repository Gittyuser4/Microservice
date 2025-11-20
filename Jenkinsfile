pipeline {
    agent any

    stages {

        stage('Build & Push Docker Image') {
            steps {
                script {

                    withDockerRegistry([credentialsId: 'docker-cred', url: '']) {

                        dir('src') {
                            sh "docker build -t adijaiswal/cartservice:latest ."
                        }

                        sh "docker push adijaiswal/cartservice:latest"
                    }
                }
            }
        }
    }
}
