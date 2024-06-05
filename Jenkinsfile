pipeline {
    agent any
    
    tools{
     maven 'maven3'
    }

    stages {
        stage('Git checkout') {
            steps {
                git branch: 'dev', url: 'https://github.com/Reshmavinu/Boardgame.git'
            }
        }
        stage('test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('build') {
            steps {
                sh 'mvn package'
            }
        }
    }
}
