pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo "Собираем проект..."'
                sh 'mkdir -p build && echo "artifact" > build/output.txt'
            }
        }
        stage('Test') {
            steps {
                sh 'echo "Запускаем тесты..."'
                sh 'cat build/output.txt | grep artifact'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo "Деплойим приложение на сервер (пока фейково)!"'
            }
        }
    }
}
