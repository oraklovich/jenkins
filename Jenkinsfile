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
        stage('Code Analysis') {
            dir('demo') {
               withSonarQubeEnv('MySonarQube') {
                  sh 'mvn sonar:sonar -Dsonar.projectKey=demo'
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
