pipeline {
    agent any
    
    options{
        timestamps()
    }
    stages {
        stage('Crear entorno EB'){
            steps {
                 withAWS(credentials: 'aws_access_key', region: 'eu-west-1') {
                    dir("proyecto") {
                        sh 'eb create mi-entorno-dev'
                    }
                 }
            }
        }
    }
}

