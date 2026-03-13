pipeline {
    agent any

    stages {

        stage('Start Nginx') {
            steps {
                sh 'sudo systemctl start nginx'
            }
        }

        stage('Deploy Website') {
            steps {
                sh '''
                sudo rm -rf /usr/share/nginx/html/*
                sudo cp -r * /usr/share/nginx/html/
                '''
            }
        }

        stage('Restart Nginx') {
            steps {
                sh 'sudo systemctl restart nginx'
            }
        }

    }
}
