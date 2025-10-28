pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/Gangadhar017/netflix-clone.git'
            }
        }
        stage('Deploy to Apache') {
            steps {
                sh '''
                sudo rm -rf /var/www/html/*
                sudo cp -r * /var/www/html/
                sudo systemctl restart httpd
                echo "Website deployed successfully!"
                '''
            }
        }
    }
}
