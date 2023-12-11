pipeline {
    agent any
 
    stages {
        stage('Install Helm') {
            steps {
                script {
                    sh 'curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/master/scripts/get-helm-3'
                    sh 'chmod 700 get_helm.sh'
                    sh './get_helm.sh'
                }
            }
        }

        stage('Run Helmfile') {
            steps {
                script {
                    sh 'sudo -u sigmoid helmfile apply'
                }
            }
        }
    }
}
