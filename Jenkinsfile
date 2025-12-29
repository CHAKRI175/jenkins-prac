pipeline {
    agent any

    stages {
        stage('Build Java App') {
            steps {
                dir('hello-world-ci/java-app') {
                    sh 'javac HelloWorld.java'
                    sh 'java HelloWorld'
                }
            }
        }

        stage('Install Node Dependencies') {
            steps {
                dir('hello-world-ci/node-app') {
                    sh 'npm init -y'
                    sh 'npm install'
                    sh 'node app.js'
                }
            }
        }
    }
}

