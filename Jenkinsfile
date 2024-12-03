pipeline {
    agent { label 'linux-node' }

    stages {
        stage('Build and Run Container') {
            steps {
                script {
                    docker.build('node-webapp:latest')
                    docker.image('node-webapp:latest').run('-d -p 3000:3000')
                }
            }
        }
    }
}
