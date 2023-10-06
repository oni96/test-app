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

       stage('Ls'){
        steps{
        //  env.NODE_ENV = "test"
         print "Environment will be : ${env.NODE_ENV}"
         sh 'ls'
         }
       }

    
}

}
