pipeline{
    agent any
    environment{

    }
    stages{
        stage("Build"){
            steps{
                sh "docker-compose build"
            }
        }
        stage("Push"){
            steps{
            sh "docker-compose push"
            }
        }
        stage("Deploy"){
            steps{
            sh "docker-compose up -d"
            }
        }
    }
}