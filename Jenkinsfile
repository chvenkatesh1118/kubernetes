pipeline {
    agent any
    stages {
        stage('pull') {
            steps {
                sh 'docker pull nginx'
            }
        }
        stage('run') {
                    steps {
                        sh 'docker run -itd -p 81:80 nginx'
                    }
                }
    }
}