pipeline {
    agent any
    stages {
        stage ('push artifact') {
            steps {
                bat 'mkdir -p archive'
                bat 'echo test > archive/test.txt'
                zip zipFile: 'db-code.zip', archive: false, dir: ''
                archiveArtifacts artifacts: 'db-code.zip', fingerprint: true
            }
        }
       }
    }