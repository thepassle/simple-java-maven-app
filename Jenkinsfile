pipeline {
    agent {
        docker {
            image 'maven:3-alpine' 
            args '-v /root/.m2:/root/.m2' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                chmod -R 755 /var/jenkins_home
                sh 'echo hello'
            }
        }
    }
}
