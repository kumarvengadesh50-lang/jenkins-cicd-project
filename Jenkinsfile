
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
                sh 'test -f index.html'
                echo 'HTML File Verified Successfully'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying Website to Nginx Server'

                sh '''
                    scp -i /var/lib/jenkins/.ssh/id_ed25519_deploy \
                    -o IdentitiesOnly=yes \
                    -o BatchMode=yes \
                    index.html ubuntu@172.31.12.22:/var/www/html/index.html
                '''

                echo 'Website Deployment Successful'
            }
        }
    }
}
