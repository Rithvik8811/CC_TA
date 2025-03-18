pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ main/hello.cpp -o hello_exec'  // Use main/hello.cpp
            }
        }
        stage('Test') {
            steps {
                sh './hello_exec'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deployment stage (simulated)'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline Failed!'
        }
    }
}
