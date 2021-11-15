pipeline 
{
          agent any
            stages {
                stage('Pull') {
                     steps{
                        script{
                            checkout([$class: 'GitSCM', branches: [[name: '*/master']],
                               userRemoteConfigs: [[
                                   credentialsId: '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',
                                   url: 'https://github.com/oumaya-khemir/first-app.git']]])
                              }
                           }
                        }
         
               stage('Install') {
             steps{
                script{
                    sh "sudo npm install"
                }
            }
        }
               
               stage ('Build') {
	
		      steps {
			 script{
			
			    sh "ansible-playbook ansible/build.yml -i ansible/inventory/host.yml"
	
			      }
			     }

	             }
               stage ('Dokcer build') {
                        steps{
                 script{
                    sh "ansible-playbook ansible/docker.yml -i ansible/inventory/host.yml "
                 }
               }

        }
               
                    }          
}
