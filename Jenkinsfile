pipeline {
    agent any

    stages {
        stage('Deploy') {
            steps {
                sh "kubectl apply -f deployment-service.yml"
            }
        }
        
        stage('Verify Deployment') {
            steps {
                sh "kubectl get svc -n webapps"
            }
        }
    }
}
