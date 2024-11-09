pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/lazarusbradley/hello-java-ant.git'
            }
        }
        stage('Setup') {
            steps {
                script {
                    env.JAVA_HOME = tool name: 'JDK 21', type: 'JDK'
                }
            }
        }
        stage('Build') {
            steps {
                sh 'ant compile'
            }
        }
        stage('Test') {
            steps {
                sh 'ant test'
            }
        }
        stage('Package') {
            steps {
                sh 'ant jar'
            }
        }
        stage('Post-Build Actions') {
            steps {
                archiveArtifacts artifacts: '**/dist/*.jar', allowEmptyArchive: true
            }
        }
    }
}
