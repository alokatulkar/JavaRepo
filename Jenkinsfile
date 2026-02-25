pipeline {
    agent any

    options {
        disableResume()
    }

    stages {
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t dockerjava .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 8082:8080 dockerjava'
            }
        }
    }
}
