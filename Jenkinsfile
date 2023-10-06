#!groovy


pipeline {
    agent{
        label 'node'
    }
 stages{
    stage('Checkout'){
          steps{
            checkout scm
            }
       }

    stage('Docker Build'){
        steps{
         sh 'docker build . -t application:latest'
         }
       }


    stage('ECR Login'){
        steps{
         sh 'aws ecr-public get-login-password --region us-east-1 | docker login --username AWS --password-stdin public.ecr.aws/y4f5w3j8'
         }
       }

       
    stage('Docker Tag'){
        steps{

         sh 'docker tag application:latest public.ecr.aws/y4f5w3j8/026-node-app:latest'
         }
       }

    stage('Docker Push'){
        steps{
         sh 'docker push public.ecr.aws/y4f5w3j8/026-node-app:latest '
         }
       }

    
}

}
