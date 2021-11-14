pipeline {

    agent any


    stages {
       stage ('Pull') {
               steps{
                 script{
                     checkout([$class: 'GitSCM', branches: [[name: '*/master']],userRemoteConfigs: [[ credentialsId: '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',url :'https://github.com/oumaya-khemir/first-app.git']]])                 
                 }

		}
        }
   }

}
