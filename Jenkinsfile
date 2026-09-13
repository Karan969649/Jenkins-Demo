pipeline {

    agent any

    stages {

        stage('Code Le Aao') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/Karan969649/Jenkins-Demo.git'
            }
        }

        stage('Docker Image Banao') {
            steps {
                sh 'docker build -t myapp .'
            }
        }

        stage('Purana Container Hatao') {
            steps {
                sh 'docker rm -f myapp-container || true'
            }
        }

        stage('Naya Container Chalao') {
            steps {
                sh 'docker run -d --name myapp-container -p 80:80 myapp'
            }
        }

    }
}
