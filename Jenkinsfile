pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/balsamrom/stage-capgemini2025.git', branch: 'main', credentialsId: 'github-cred'
            }
        }

        stage('Run Script') {
            steps {
                bat 'python hello.py'
            }
        }
    }
}
