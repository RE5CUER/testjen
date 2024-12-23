pipeline {
    agent any
    stages {
        stage('Install MySQL Client') {
            steps {
                script {
                    // Здесь уточняем замыкание с параметром, чтобы исключить неоднозначность
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
