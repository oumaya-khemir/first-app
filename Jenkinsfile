pipeline {

    agent any


    stages {
       stage ('Pull') {
               steps{
                 script{
                     checkout([$class: 'GitSCM', branches: [[name: '*/main']],userRemoteConfigs: [[ credentialsId: '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',url :'https://github.com/oumaya-khemir/first-app.git']]])                 
                 }

		}
        }
   }

}
