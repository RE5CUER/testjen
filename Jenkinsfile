pipeline {
    agent any
    stages {
        stage('Install MySQL Client') {
            steps {
                script {
                    // Команда будет выполняться с правами root через sudo
                    sh 'sudo apt-get update && sudo apt-get install -y mariadb-client'
                }
            }
        }
        stage('Run SQL Query') {
            steps {
                script {
                    // Логика SQL запроса
                }
            }
        }
    }
}
