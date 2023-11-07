pipeline {
    agent {
        docker {
            image 'node:18.18.0-alpine3.18' 
            args '-p 2376:2376' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'npm install' 
            }
        }
    }
}
