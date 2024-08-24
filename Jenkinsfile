pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/robinsingh1912/simple-express-server.git'
            }
        }
        stage('Test') {
            steps {
                sh 'npm install'
                sh 'ng test'
            }
        }
        stage('Build') {
          steps {
            sh 'ng build'
          }
        }
        stage('Deploy') {
            steps {
                bat 'move dist\\ngrx-task\\*.* C:\\nginx\\'
            }
        }
    }
}
