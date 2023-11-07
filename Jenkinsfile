pipeline {
    agent {
        docker {
            image 'docker:dind' // Use an agent image that includes Docker
            args '-p 3000:3000' 
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'docker pull jenkins/agent:latest'
                sh 'docker pull node:18.18.0-alpine3.18' // Pull the required Docker image
                sh 'docker run -p 3000:3000 -d node:18.18.0-alpine3.18' // Run your application in a Docker container
                sh 'npm install' 
            }
        }
    }
}
