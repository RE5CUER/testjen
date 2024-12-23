pipeline {
    agent any
    stages {
        stage('Install MySQL Client') {
            steps {
                script {
                    // Исправленный блок, чтобы он явно был идентифицирован как замыкание
                    sh "sudo apt-get update && sudo apt-get install -y mariadb-client"
                }
            }
        }
        stage('Run SQL Query') {
            steps {
                script {
                    // Ваш SQL-запрос здесь
                }
            }
        }
    }
}
