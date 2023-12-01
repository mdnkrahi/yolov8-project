pipeline {
    agent any

    stages {
        stage('cloning git') {
            steps {
                sh 'git clone https://github.com/mdnkrahi/yolov8.git'
            }
        }
        stage('Moving file') {
            steps {
                sh 'mv yolov8/Dockerfile Dockerfile && rm -r yolov8'
            }
        }
        stage('buld') {
            steps {
                sh 'docker build -t yolov8 .'
            }
        }
    }
}
