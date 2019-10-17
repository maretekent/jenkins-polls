pipeline {
    agent { docker { image 'python:3.6.5' } }
    environment {
        scmUrl = "git@github.com:maretekent/jenkins-polls.git"
    }
    stages {
        stage('Checkout') {
            steps {
                git url: "https://github.com/maretekent/jenkins-polls.git",
                    branch: "master",
                    credentialsId: "github"
            }
        }
        stage('Setup') {
            steps {
                script {
                    sh "echo \"Setup done here\""
                }
            }
        }
        stage('Lint') {
            steps {
                script {
                    sh "echo \"Linting done here\""
                }
            }
            
        }
        stage('Test') {
            steps {
                script {
                    sh "echo \"tests run here\""
                }
            }
        }
        stage('Build') {
            steps {
                script {
                    sh 'python --version'
                    sh "echo \"Build image push done here \""
                }
            }
            
        }
        stage('Docker Push') {
            steps {
                script {
                    sh "echo \"Docker image push done here \""
                }
            }
        }
    }
}
