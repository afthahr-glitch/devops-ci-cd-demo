pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                git branch: 'main',
                url: 'https://github.com/your-username/your-repo.git'
            }
        }

        stage('Setup') {
            steps {
                echo 'Installing dependencies...'
                sh 'python3 -m pip install flask || true'
            }
        }

        stage('Run App Test') {
            steps {
                echo 'Starting Flask app test...'
                sh 'python3 app.py &'
            }
        }
    }
}
