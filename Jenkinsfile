pipeline {
    agent { label 'Jenkin-Agent' }
    tools {
        jdk 'jdk17'
        maven 'Maven3'
    }
    stages {
        stage('workspace cleanup') {
            steps {
                cleaanWs()
            }
        }
    
        stage('Checkout') {
            steps {
                 git branch: 'main', credentialsId: 'git-pat', url: 'https://github.com/charan23199/registration-app.git'
            }
        }
    }
}

   
