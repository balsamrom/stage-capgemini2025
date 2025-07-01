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
    
    post {
        success {
            echo '✅ Build terminé avec succès !'
        }
        failure {
            echo '❌ Échec du build ! Vérifiez les logs.'
        }
        always {
            echo '📦 Pipeline terminé.'
        }
    }
}
