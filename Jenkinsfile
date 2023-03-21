 pipeline  {
 	agent: any
 	stages {
 		
		stage("git-clone-repo"){
 			steps{
				sh "sudo git clone -b mumbai https://github.com/rohaanuv/jenkins-docker-int.git mumbai" 				
 				sh "sudo git clone -b pune https://github.com/rohaanuv/jenkins-docker-int.git pune" 
                sh "sudo git clone -b nagpur https://github.com/rohaanuv/jenkins-docker-int.git nagpur"
                
 			}
 		}
		stage("Ansible running"){
 			steps{
				sh '''
                    su ron 
                    ansible-playbook main.yml
                '''
               
 			}
 		}
		
 		
 	}
 }
 
