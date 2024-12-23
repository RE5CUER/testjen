pipeline {
    agent any
    stages {
        stage('Install MySQL Client') {
            steps {
                script {
                    // Устанавливаем sudo
                    sh 'apt-get update && apt-get install -y sudo'
                    // Далее устанавливаем MySQL клиент
                    sh 'sudo apt-get update && sudo apt-get install -y mariadb-client'
                }
            }
        }
        stage('Run SQL Query') {
            steps {
                script {
                    echo 'Running SQL query'
                }
            }
        }
    }
}
