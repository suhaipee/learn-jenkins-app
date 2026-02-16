pipeline {
    agent any

    stages {
        stage('Build') {
            agent {
                docker {
                    image 'maven:3.8.4-openjdk-17'
                    reuseNode true
                }
            }
            steps {
                sh '''
                    ls -la
                    node --version
                    npm --version
                    npm ci
                    npm run build
                    ls -la
                '''
            }   
        }
    }
}
