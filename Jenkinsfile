pipeline {
    agent any

    stages {
        stage('Build & Push Docker Image') {
            steps {
                script {
                    withDockerRegistry([credentialsId: 'docker-cred', url: '']) {

                        
                            sh "docker build -t prabhalasubbu99/recommendationservice:latest ."
                        

                        sh "docker push prabhalasubbu99/recommendationservice:latest"
                    }
                }
            }
        }
    }
}
