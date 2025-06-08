pipeline {
    agent any

    tools {
        maven 'Maven' // Make sure this name matches Jenkins Maven installation
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/KRISHNA-MS17/jenkinsmaven.git'
            }
        }

        stage('Build') {
            steps {
                bat 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                bat 'mvn test'
            }
        }

        stage('Run Application') {
            steps {
                bat 'java -jar target/jenkinsmaven-0.0.1-SNAPSHOT.jar'
            }
        }
    }
}
