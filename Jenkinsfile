pipeline {
    agent any

    stages {
        stage('Login to Docker Hub') {
            steps {
                script {
                    withCredentials([usernamePassword(credentialsId: 'docker-hub-credentials', passwordVariable: 'DOCKER_PASSWORD', usernameVariable: 'DOCKER_USERNAME')]) {
                        docker.withRegistry('https://index.docker.io/v1/', DOCKER_USERNAME, DOCKER_PASSWORD) {
                            // Perform any Docker-related actions here after logging in
                            // For example: docker.pull('your-image:tag')
                        }
                    }
                }
            }
        }
    }
}
