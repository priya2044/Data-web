pipeline {
    agent any
    stages{
        stage("Code Clone"){
            steps{
            git url:"https://github.com/priya2044/Data-web.git", branch: "main"
        }
        }
        stage("Code Build"){
            steps{
            sh "docker build . -t data-web-app"
        }
        }
        stage("Code Run"){
            steps{
            sh "docker run -d -p 80:80 data-web-app"
        }
        }
        }
    }
