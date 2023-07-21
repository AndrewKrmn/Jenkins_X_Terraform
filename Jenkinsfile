pipeline {
    agent any

    stages {
        stage('git clone') {
            steps {
                sh '''
                rm -rf terraform_X_Jenkins
                git clone https://github.com/skalajonson/terraform_X_Jenkins.git
                '''
            }
        }
        stage('run durka') {
            steps {
                sh '''
                cd terraform_X_Jenkins/
                terraform init
                terraform validate
                terraform apply -auto-approve
                '''
            }
        }
    }
}
