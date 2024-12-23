pipeline {
    agent any
    stages {
        // Этап установки клиента MySQL
        stage('Install MySQL Client') {
            steps {
                script {
                    // Установка mysql client в контейнер Jenkins
                    sh 'apt-get update && apt-get install -y mysql-client'
                }
            }
        }
        // Этап выполнения SQL запроса
        stage('Run SQL Query') {
            steps {
                script {
                    echo 'Executing SQL script...'
                    sh '''
                    # Выполняем запрос к базе данных
                    mysql --user=rfamro --host=mysql-rfam-public.ebi.ac.uk --port=4497 --database=Rfam -e "SELECT VERSION();"
                    '''
                }
            }
        }
    }
}
