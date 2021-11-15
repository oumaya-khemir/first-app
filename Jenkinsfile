pipeline {

    agent any


    stages {
       stage ('GIT') {
               steps{
                 script{
                     checkout([$class: 'GitSCM', branches: [[name: '*/master']],userRemoteConfigs: [[ credentialsId: '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',url :'https://github.com/oumaya-khemir/first-app.git']]])                 
                 }

		}
        }
        stage ('Build') {
               steps{
                 script{
                    sh "ansible-playbook ansible/build.yml -i ansible/inventory/host.yml "
                 }
               }

        }
        
     


   }

}
