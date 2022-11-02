pipeline {
    agent any
    stages {
        stage ('push artifact') {
            steps {
                
                zip zipFile: 'db-code.zip', archive: false, dir: ''
                archiveArtifacts artifacts: 'db-code.zip', fingerprint: false
            }
        }
       }
    }