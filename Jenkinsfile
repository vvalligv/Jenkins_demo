pipeline {
    agent any

    stages {
        
        stage('Install Dependencies') {
            steps {
                sh 'pip3 install --break-system-packages -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
              sh 'python3 -m pytest test_app.py'
            }
        }

        stage('Deploy') {
            steps {
                sh 'python3 app.py'
            }
        }
    }
}
