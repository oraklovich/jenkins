pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                dir('demo') {
                    sh 'mvn clean package'
                }
            }
        }
        stage('Test') {
            steps {
                dir('demo') {
                    sh 'mvn test'
                }
            }
        }
        stage('Deploy') {
            steps {
                echo 'Деплойим артефакт!'
                dir('demo') {
                    sh 'ls -la target/'
                }
            }
        }
    }
}
