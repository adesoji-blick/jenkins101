pipeline {
    agent any

    stages {
        stage ('List repo content') {
            when {
                branch "master"
            }
            steps {
               sh "ls -ltr"
            }
        }
        stage ('create email directory on target machine') {
            steps {
               sh "mkdir -p /tmp/emails/others"
            }
        }

        stage ('copy file from downloaded repo to dest') {
            steps {
               sh "cp hotmail.txt  /tmp/emails/others"
            }
        }
    }
}