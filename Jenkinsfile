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
        stage('Test') {
            steps {
                sh "echo Setting POM Version"
                sh "mvn -v"
                sh "mvn build-helper:parse-version versions:set '-DnewVersion=\${parsedVersion.majorVersion}.\${parsedVersion.minorVersion}.\${parsedVersion.nextIncrementalVersion}' versions:commit"
            }
        }
        stage('Bla') { 
            steps {
                sh 'echo BLABLABLABALBLABAL'
            }
        }
    }
}

sh "curl -v --user user:password --data-binary ${buildDir}package${env.BUILD_NUMBER}.tar -X PUT \"http://artifactory.mydomain.com/artifactory/release-packages/package${env.BUILD_NUMBER}.tar\""
