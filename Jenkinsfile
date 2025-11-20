pipeline {
    agent any

    stages {
        stage('Build & Push Docker Image') {
            steps {
                script {
                    withDockerRegistry([credentialsId: 'docker-cred', url: '']) {

                        dir('src') {
                            sh "docker build -t prabhalasubbu99/cartservice:latest ."
                        }

                        sh "docker push prabhalasubbu99/cartservice:latest"
                    }
                }
            }
        }
    }
}
