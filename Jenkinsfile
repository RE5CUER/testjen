pipeline {
    agent any
    stages {
        stage('Install MySQL Client') {
            steps {
                script {
                    // Устанавливаем MySQL client
                    sh "sudo apt-get update && sudo apt-get install -y mariadb-client"
                }
            }
        }
        stage('Run SQL Query') {
            steps {
                script {
                    // Выполняем SQL-запрос
                    echo 'Running SQL query'
                    // Здесь ваш SQL запрос или другие команды
                }
            }
        }
    }
}
