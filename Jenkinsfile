pipeline {
    agent any
    stages {
        stage ('push artifact') {
            steps {
                bat 'mkdir archive'
                bat 'echo test > archive/test.txt'
                zip zipFile: 'db-code.zip', archive: false, dir: 'archive'
                archiveArtifacts artifacts: 'db-code.zip', fingerprint: true
            }
        }
       }
    }