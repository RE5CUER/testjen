pipeline {
    agent any
    stages {
        stage('Install MySQL Client') {
            steps {
                script('script block') {
                    sh "sudo apt-get update && sudo apt-get install -y mariadb-client"
                }
            }
        }
        stage('Run SQL Query') {
            steps {
                script('script block') {
                    // Ваш SQL-запрос здесь
                }
            }
        }
    }
}
