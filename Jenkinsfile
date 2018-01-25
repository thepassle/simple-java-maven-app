pipeline {
    agent any
    stages {
        stage('Build') { 
            steps {
                sh 'echo Starting build'
                sh 'mvn -v'
                sh 'mvn test'
            }
        }
        stage('Test'){
            steps{
                sh "echo Setting POM version"
                sh "mvn -v"
                sh "#!/bin/bash echo 'hello world'"
            }
        }
        stage('Bla') { 
            steps {
                sh 'echo BLABLABLABALBLABAL'
            }
        }
    }
}

