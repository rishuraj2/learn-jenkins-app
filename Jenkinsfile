pipeline {
    agent any

    stages {
        stage('w/o docker') {
            steps {
                echo "without doker"
            }
        }

        stage('w/ docker') {
            agent {
                docker {
                    image 'node:18-alpine'
                }
            }
            steps {
                echo "with docker"
                sh 'npm --version'
            }
        }
    }
}