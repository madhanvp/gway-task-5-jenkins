pipeline {
    agent any

    stages {
        stage('Pull Code') {
            steps {
                git branch: 'main', url: 'https://github.com/madhanvp/gway-task-5-jenkins.git'
            }
        }

        stage('Build Image') {
            steps {
                sh 'docker build -t gway-jenkins-app .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d --name gway-jenkins-app -p 8082:80 gway-jenkins-app'
            }
        }
    }
}
