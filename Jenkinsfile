pipeline {
    agent any

    environment {
        DB_HOST = 'mysql-rfam-public.ebi.ac.uk'
        DB_USER = 'rfamro'
        DB_PASSWORD = ''  //без пароля
        DB_PORT = '4497'
        DB_NAME = 'Rfam'
    }

    stages {
        stage('Checkout SQL Script') {
            steps {
                git branch: 'main', url: 'https://github.com/RE5CUER/testjen.git'
            }
        }

        stage('Run MySQL Query') {
            steps {
                script {
                    sh '''#!/bin/bash
                    mysql --user=$DB_USER --host=$DB_HOST --port=$DB_PORT --database=$DB_NAME -e "select * from fr.fram_acc limit 1;"
                    mysql --user=$DB_USER --host=$DB_HOST --port=$DB_PORT --database=$DB_NAME -e "SELECT fr.rfam_acc, fr.rfamseq_acc, fr.seq_start, fr.seq_end FROM full_region fr, rfamseq rf, taxonomy tx WHERE rf.ncbi_id = tx.ncbi_id AND fr.rfamseq_acc = rf.rfamseq_acc AND tx.ncbi_id = 10116 AND is_significant = 1;"
                    '''
                }
            }
        }
    }

    post {
        always {
            echo "Pipeline completed."
        }
    }
}
