 pipeline  {
 	agent any
 	stages {
 		
		stage("git-clone-repo"){
			dir('/mnt/') {
 			steps{
				sh "sudo git clone -b mumbai https://github.com/rohaanuv/jenkins-ansible-int-static.git mumbai" 				
 				sh "sudo git clone -b pune https://github.com/rohaanuv/jenkins-ansible-int-static.git pune" 
                sh "sudo git clone -b nagpur https://github.com/rohaanuv/jenkins-ansible-int-static.git nagpur"
				 sh "sudo git clone https://github.com/rohaanuv/jenkins-ansible-int-static.git "
                
 			}
			}
			}
		stage("Ansible running"){
 			dir('/mnt/jenkins-ansible-int-static/') {
			steps{
				sh '''
                    su ron 
                    ansible-playbook main.yml
                '''
               
 			}
			}
 		}
		
 		
 	}
 }
 
