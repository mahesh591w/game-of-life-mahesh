pipeline {

	agent {
				label {
				
				
				label "Built-In"
				customWorkspace "/mnt/project"
				
				}
	}
	
	stages {
		
			stage ('git-gameoflife') {
				
					steps {  
								sh "sudo cd /mnt/project && rm -rf *"
								
								
								sh "git clone https://github.com/mahesh591w/game-of-life-mahesh.git"
								sh "rm -rf /root/.m2/repository/"
								
								sh "mvn clean install"
								sh "scp -i /mnt/New-aws.pem gameoflife-web/target/gameoflife.war ec2-user@172.31.44.26:/mnt/web-sever/apache-tomcat-9.0.71"
								
						}
			
					}
					
			
	}
}
