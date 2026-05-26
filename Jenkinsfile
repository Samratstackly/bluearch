pipeline {
    agent any

    stages {

        stage('Clone Repository') {
            steps {
                git 'https://github.com/USERNAME/bluearch-website.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Building Website...'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing Website...'
            }
        }

        stage('Deploy') {
            steps {
                sh '''
                sudo cp -r * /var/www/html/
                '''
            }
        }
    }

    post {
        success {
            echo 'Deployment Successful!'
        }

        failure {
            echo 'Deployment Failed!'
        }
    }
}
