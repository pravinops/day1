pipeline {
    agent {
        docker { image 'node:20.18.0-alpine3.20' }
    }
    stages {
        stage('Testing') {
            steps {
                sh 'node --version'
            }
        }
    }
}
