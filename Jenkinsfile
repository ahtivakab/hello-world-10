pipeline {
    agent any
        tools {
    maven 'Maven'
    }
    stages {
        stage('GIT Checkout') {
            steps {
                git changelog: false, credentialsId: 'b31ee1ac-798b-4389-b78b-3752cb9bbc2d', poll: false, url: 'https://github.com/ahtivakab/hello-world-war.git'
            }
        }
        stage('Execute Shell') {
            steps {
               sh 'echo "WELCOME TO THIS PAGE"'
            }
        }
        stage('Build MAVEN') {
            steps {
                sh 'mvn clean install'
            }
        }
    }
}
