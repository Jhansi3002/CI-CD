cat > Jenkinsfile <<EOF
pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build Docker image') {
            steps {
                sh 'docker build -t jenkins-python-app .'
            }
        }
        stage('Run Docker container') {
            steps {
                sh 'docker run --rm jenkins-python-app'
            }
        }
    }
}
EOF
