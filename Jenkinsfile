pipeline {
    agent any

    parameters {
        credentials(name: 'DOCKER_CREDENTIALS', credentialType: 'com.cloudbees.plugins.credentials.impl.UsernamePasswordCredentialsImpl') 
    }

    stages {
        stage('Build') {
            steps {
                script {
                    docker.withRegistry('https://index.docker.io/v1/', DOCKER_CREDENTIALS) {
                        // Your Docker-related pipeline steps here
                    }
                }
            }
        }
    }
}
