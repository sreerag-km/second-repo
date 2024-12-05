pipeline {
    agent any
    stages {
        stage("1. This is first stage") {
            steps {
                echo "This is the first stage in Declarative pipeline code"
                sh "mkdir -p abc"
                sh "touch abc/script.txt"
                writeFile file: "abc/suresh.txt", text: "This is the test file created"
                writeFile file: "abc/sunil.txt", text: "This is the first stage in Declarative pipeline code"
                echo "Print the number of files in the folder"
                sh "ls -alrts abc"
            }
        }
        stage("2. Update and install some packages") {
            steps {
                echo "This is the second stage"
                sh "sudo yum update -y"
                sh "sudo yum install -y docker tree"
                sh "sudo systemctl restart docker"
                sh "sudo systemctl enable docker"
                sh "sudo systemctl status docker"
            }
        }
        stage("3. Checking system properties") {
            steps {
                echo "This is the third stage"
                sh "date"
                sh "cal 2025"
                sh "uptime"
                sh "df -h"
                sh "free -m"
                sh "iostat"
                sh "tree /"
            }
        }
        stage("4. Creating some files and folders") {
            steps {
                sh "mkdir -p incoming"
                sh "mkdir -p outgoing"
                writeFile file: "incoming/suresh.txt", text: "This is the test file created"
                writeFile file: "outgoing/suresh.txt", text: "This is the test file created"
                sh "last"
            }
        }
    }
}
