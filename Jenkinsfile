
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Build Stage Started'
                echo 'Application Build Successful'
            }
        }

        stage('Test') {
            steps {
                echo 'Test Stage Started'
                sh 'git --version'
                echo 'Testing Completed Successfully'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploy Stage Started'
                echo 'Demo Deployment Successful'
            }
        }
    }
}
