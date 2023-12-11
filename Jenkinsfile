pipeline {
    agent any

    stages {
        stage('Install Helm and Helmfile') {
            steps {
                script {
                    sh 'helm version'
                    sh 'helmfile init'
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