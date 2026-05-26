pipeline {
    agent any

    stages {

        stage('Checkout Code') {
            steps {
                git branch: 'main',
                url: 'https://github.com/Samratstackly/bluearch.git'
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
