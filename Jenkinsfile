pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o PES2UG22CS231 main/hello.cpp'
                echo 'Build stage completed successfully'
            }
        }
        
        stage('Test') {
            steps {
                sh './PES2UG22CS231'
                echo 'Test stage completed successfully'
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deployment stage completed successfully'
                echo 'Deployed the application'
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed'
        }
        success {
            echo 'Pipeline executed successfully'
        }
    }
}
