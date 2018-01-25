pipeline {
    agent any
    stages {
        stage('Build') { 
            steps {
                sh 'echo hesadfsadsadsaddsfllo'
                sh 'mvn -v'
                sh 'mvn test'
                sh 'mvn build-helper:parse-version versions:set -DnewVersion=\${parsedVersion.majorVersion}.\${parsedVersion.minorVersion}.\${parsedVersion.nextIncrementalVersion} versions:commit'
            }
        }
        stage('Bla') { 
            steps {
                sh 'echo BLABLABLABALBLABAL'
            }
        }
    }
}

