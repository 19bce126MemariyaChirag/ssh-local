pipeline {
    agent {
        docker { image 'node:16-alpine' }
    }
    environment {
        APP_NAME = "unit-testing-asp-.net-core-gitlav-vs-jenkins "
        APP_PORT = "5000"
        IMAGE_TAG = "latest"
        DOCKER_REGISTRY="memariyachirag126"
        DOCKER_USERNAME="memariyachirag126"
        DOCKER_PASSWORD="dckr_pat_QUWempv4V6X7lbUR-UU83Y0lIdo"
        }
    stages {
        stage('Test') {
            steps {
                sh 'node --version'
            }
        }
        stage('Build') {
            steps {
                // Build the project
                sh 'dotnet build'
            }
        }
        stage('test') {
            steps {
                // test the project
                sh 'dotnet test'
            }
        }
        stage('pulbish'){
            steps{
                // Publish the project
                sh 'dotnet publish -c Release -o ./publish'
            }
        }
        stage('Docker Build') {
            steps {
                // Build Docker image
                script {
                    docker.build("${DOCKER_REGISTRY}/${APP_NAME}:${IMAGE_TAG}", "--build-arg APP_PORT=${APP_PORT} .")
                }
            }
        }
    }
}
