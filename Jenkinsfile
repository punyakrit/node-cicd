pipeline {
    agent any
    
    stages{
        stage("Code"){
            steps{
                git url: "https://github.com/punyakrit/node-cicd/", branch: "master"
            }
        }
        stage("Build & Test"){
            steps{
                sh "docker build -t punyakrit/node1234567 ."
                sh "docker run -p 8000:8000 -d -it punyakrit/node1234567"
            }
        }
        
    }
}
