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
        //  env.NODE_ENV = "test"
         print "Environment will be : ${env.NODE_ENV}"
            sh 'whoami'
         sh 'docker build . -t application:latest'
         }
       }

    
}

}
