pipeline {
    agent any
    stages {
        stage('Install MySQL Client') {
            steps {
                script {
                    // Добавляем явный параметр 'it ->' для правильной обработки замыкания
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
