pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/KotaShriya/PES1UG22CS290_Jenkins'
            }
        }
        stage('Build') {
            steps {
                sh 'make -C main'
            }
        }
        stage('Test') {
            steps {
                sh './main/hello_exec'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying the build...'
            }
        }
    }
    
    post {
        failure {
            echo 'pipeline failed'
        }
    }
}
