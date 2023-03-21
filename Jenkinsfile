 pipeline  {
 	agent any
 	stages {
 		
		stage("git-clone-repo"){
			
 			steps{
				sh "sudo git clone -b mumbai https://github.com/rohaanuv/jenkins-ansible-int-static.git mumbai" 				
 				sh "sudo git clone -b pune https://github.com/rohaanuv/jenkins-ansible-int-static.git pune" 
                sh "sudo git clone -b nagpur https://github.com/rohaanuv/jenkins-ansible-int-static.git nagpur"
				 sh "sudo git clone https://github.com/rohaanuv/jenkins-ansible-int-static.git "
                
 			
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
 
