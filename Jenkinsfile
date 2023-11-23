pipeline {
    agent any
    environment {
        MYSQL_ROOT_PASSWORD = credentials("MYSQL_ROOT_PASSWORD")
    }
  
    stages {
        stage('Deploy') {
            steps {
                sh '''
                kubectl apply -f frontend.yaml
                kubectl apply -f backend.yaml
                sleep 60
                kubectl get services
                '''
            }

        }

    }

}

