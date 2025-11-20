pipeline {
    agent any

    stages {
        stage('Build & Push Docker Image') {
            steps {
                script {
                    withDockerRegistry([credentialsId: 'docker-cred', url: '']) {
                            sh "docker build -t prabhalasubbu99/cartservice:latest ."
                            sh "docker push prabhalasubbu99/cartservice:latest"
                    }
                }
            }
        }
    }
}
