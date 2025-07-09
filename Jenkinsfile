pipeline {
    agent any
    
    stages {
        stage('CHECKOUT') {
            steps {
                git 'https://github.com/akshay1996137/jenkins-java-project.git'
            }
        }
        stage('BUILD') {
            steps {
                sh 'mvn compile'
            }
        }
        stage('TEST') {
            steps {
                sh 'mvn test'
            }
        }
        stage('ARTIFACT') {
            steps {
                sh 'mvn package'
            }
        }
        stage ('deploy') {
            input {
                message "is your inputs correct ?"
                ok "yes"
            }
            steps {
                echo "my code is deployed"
            }
        }
    }
}
