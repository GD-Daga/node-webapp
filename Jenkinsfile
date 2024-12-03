pipeline {
    agent {  
        label 'linux-node'  
    }  
    stages {
        stage('Build Image') {
            steps {  
                script {  
                    docker.build('node-webapp:latest')
                }
            }  
        }  
        stage('Run Container') {
            steps {  
                script {  
                    docker.image('node-webapp:latest').run('-d -p 3000:3000')
                }  
            }  
        }
    }  
}

