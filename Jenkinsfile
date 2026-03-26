pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'docker build -t my-project:latest .'
            }
        }
        stage('Test') {
            steps {
                sh 'pytest tests/'  // adjust if you have tests
            }
        }
        stage('Deploy') {
            steps {
                sh 'docker run -d -p 5000:5000 my-project:latest'
            }
        }
    }
}
