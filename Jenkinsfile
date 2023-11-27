pipeline {
    agent { label 'tiger-label' }
    tools {
        jdk 'jdk17'
        maven 'maven3'
    }
    stages {
        stage('workspace-cleanup') {
            steps {
                cleanWs()
            }
        }
    
        stage('Checkout') {
            steps {
                 git branch: 'main', credentialsId: 'git-pat', url: 'https://github.com/charan23199/registration-app.git'
            }
        }
         stage('Build- =Application') {
            steps {
                 sh 'mvn clean package'
            }
        }
    }
}

   
