pipeline {
    agent any
    
    environment {
        DATE = "21.04.2023"
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building process...'
                sh '''
                cat test.py
                '''
            }
        }
        stage('Test') {
            steps {
                echo 'Testing process...'
                sh '''
                python3 --version
                python3 test.py
                '''
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deployment process...'
                sh '''
                cat req.txt | grep text
                
                '''
                echo "Today is ${env.DATE}"
            }
        }
    }
}