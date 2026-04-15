pipeline {
    agent any
    triggers {
        githubPush() // This listens for the webhook signal
    }
    stages {
        stage('Install Dependencies') {
            steps {
                sh 'pip3 install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'python3 -m unittest'
            }
        }
    }
}
