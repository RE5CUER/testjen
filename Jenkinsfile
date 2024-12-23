pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                // Скачиваю файлы из репозитория
                git url: 'https://github.com/RE5CUER/testjen', branch: 'main'
            }
        }
        stage('Run SQL Query') {
            steps {
                script {
                    // SQL-запрос
                    echo "Executing SQL script..."
                    
                    sh '''
                    #Проверяю подключение
                    mysql --user=rfamro --host=mysql-rfam-public.ebi.ac.uk --port=4497 --database=Rfam -e "SELECT VERSION();"
                    
                    #Выполняю запрос query.sql
                    mysql --user=rfamro --host=mysql-rfam-public.ebi.ac.uk --port=4497 --database=Rfam < query.sql > result.txt
                    
                    #Показать результат
                    cat result.txt
                    '''
                }
            }
        }
    }
    post {
        always {
            echo "Pipeline completed."
        }
        success {
            echo "YEAHH! Pipeline completed successfully!"
        }
        failure {
            echo "F***K! Pipeline failed!"
        }
    }
}
