pipeline {
    agent any

    stages {
        stage ('List repo content') {
            steps {
               sh "ls -ltr"
            }
        }
        stage ('create email directory on target machine') {
            steps {
               sh "mkdir -p /tmp/emails/others"
            }
        }
        // if it is master branch, copy email.txt to /tmp/emails   
        stage ('manage yahoomail account') {
            when {
                branch "master"
            }
            steps {
               sh "cp emails.txt  /tmp/emails/"
            }
        }
         // if it is gmail branch, copy gmail.txt to /tmp/emails/others  
        stage ('manage gmail account') {
            when {
                branch "gmail"
            }
            steps {
               sh "cp gmail.txt  /tmp/emails/others"
            }
        }
        // if it is hotmail branch, copy hotmail.txt to /tmp/emails/others  
        stage ('manage hotmail account') {
            when {
                branch "hotmail"
            }
            steps {
               sh "cp hotmail.txt  /tmp/emails/others"
            }
        }  
        // if it is twitter branch, copy twitter.txt to /tmp/emails/others  
        stage ('manage twitter account') {
            when {
                branch "twitter"
            }
            steps {
               sh "cp twitter.txt  /tmp/emails/others"
            }
        }     
    }
}