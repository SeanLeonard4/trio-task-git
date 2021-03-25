pipeline{
    agent any
    environment{
        DOCKERHUB_PASSWORD = credentials("DOCKERHUB_PASSWORD")
    }
    stages{
        // stage("install dependencies"){
        //     steps{
        //         sh "bash install-dependencies.sh"
        //     }
        // }
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