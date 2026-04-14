pipeline {
    agent any

    environment {
        DOCKER_IMAGE = "Sagar08082004/docker-demo"
    }

    stages {

        stage('Clone Code') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/SagarNajardhane/DevOps_Assingment_8A.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t %DOCKER_IMAGE% .'
            }
        }

        stage('Login to Docker Hub') {
            steps {
                bat 'docker login -u Sagar08082004 -p dckr_pat_5qub4DyZukWwVjbBi5zCfGB_dP0D'
            }
        }

        stage('Push Docker Image') {
            steps {
                bat 'docker push %DOCKER_IMAGE%'
            }
        }
    }
}
