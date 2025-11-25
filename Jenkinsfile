pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/vvalligv/Jenkins_demo.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'pip install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'pytest test_app.py'
            }
        }

        stage('Deploy') {
            steps {
                sh 'python app.py'
            }
        }
    }
}
