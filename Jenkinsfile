pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                script {
                    // Create and activate a virtual environment
                    sh 'python3 -m venv venv'
                    sh 'source venv/bin/activate'

                    // Install dependencies using pip within the virtual environment
                    sh 'pip3 install -r myapp/requirements.txt'
                }
            }
        }

        stage('Test') {
            steps {
                // Add your test steps here
            }
        }

        stage('Deliver') {
            steps {
                // Add your delivery steps here
            }
        }
    }

    post {
        always {
            // Deactivate the virtual environment after the pipeline
            sh 'deactivate'
        }
    }
}
