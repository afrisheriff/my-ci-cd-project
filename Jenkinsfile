pipeline {
    agent any

    stages {

        stage('Clone Code') {
            steps {
                git 'https://github.com/afrisheriff/my-ci-cd-project.git'
            }
        }

        stage('Install Dependencies') {
            steps {
               sh 'pip3 install -r requirements.txt'
            }
        }

        stage('Build Docker Image') {
            steps {
               sh 'docker build -t my-app .'
            }
        }

        stage('Run Container') {
            steps {
               sh 'docker run -d -p 5000:5000 my-app'
            }
        }
    }  
