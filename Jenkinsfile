pipeline {
    agent any
    stages {
        stage ('push artifact') {
            steps {
                bat 'del *.zip'
                zip zipFile: 'db-code.zip', archive: false, dir: ''
                archiveArtifacts artifacts: 'db-code.zip', fingerprint: false
            }
        }
       }
    }