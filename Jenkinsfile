pipeline {
    agent any

    stages {
        stage('Build & Push Docker Image') {
            steps {
                script {
                    withDockerRegistry([credentialsId: 'docker-cred', url: '']) {

                        
                            sh "docker build -t prabhlasubbu99/loadgenerator:latest ."
                        

                        sh "docker push prabhalasubbu99/loadgenerator:latest"
                    }
                }
            }
        }
    }
}
