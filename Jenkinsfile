pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/Wiami/riskamis.git'
            }
        }

        stage('Execute') {
            steps {
                bat 'ant blob'
            }
        }
    }
    post {
        success {
            echo 'Успешно выполнен'
        }
        failure {
            echo 'Провал'
        }
    }
}
