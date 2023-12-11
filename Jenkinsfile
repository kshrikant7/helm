pipeline {
    agent any

    stages {
        stage('Install Helm and Helmfile') {
            steps {
                script {
                    sh 'helm version'
                    sh 'helmfile --version'
                }
            }
        }

        stage('Deploy with Helmfile') {
            steps {
                script {
                    sh 'helmfile apply'
                }
            }
        }
    }
}