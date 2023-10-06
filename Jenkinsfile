#!groovy


pipeline {
    agent{
        label 'node'
    }
 stages{
       stage('Checkout'){
          checkout scm
       }

       stage('Ls'){
         env.NODE_ENV = "test"
         print "Environment will be : ${env.NODE_ENV}"
         sh 'ls'
       }

    
}

}
