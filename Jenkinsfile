pipeline {
    agent any

    stages {
        stage('Deploy') {
            steps {
                sh """
                export KUBECONFIG=/home/ubuntu/.kube/config
                kubectl apply -f deployment-service.yml
                """
            }
        }
        
        stage('Verify Deployment') {
            steps {
                sh """
                export KUBECONFIG=/home/ubuntu/.kube/config
                kubectl get svc -n webapps
                """
            }
        }
    }
}
