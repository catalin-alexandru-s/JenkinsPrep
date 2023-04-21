pipeline {
    agent any
    
    environment {
        DATE = "19.04.2023"
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building process...'
                sh '''
                cat > req.txt
                '''
            }
        }
        stage('Test') {
            steps {
                echo 'Testing process...'
                sh '''
                echo "some text here" > req.txt
                python3 --version
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