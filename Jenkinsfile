pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                git branch: 'main', url: 'https://github.com/atulkamble/pythonhelloworld.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    dockerImage = docker.build('python-hello-world')
                }
            }
        }

        stage('Run Container') {
            steps {
                script {
                    dockerImage.run()
                }
            }
        }
    }
}
