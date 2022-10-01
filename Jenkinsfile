pipeline {
		agent {
		node {
		label ('built-in')
	}
	}
	
		stages {
		
			stage ('clone-22Q1') {
			steps {
			dir ('/mnt/22Q1') {
			sh "git clone https://github.com/ronitunale/assignment1.git -b 22Q1"
			sh "chmod -R 777 /mnt/22Q1"
			sh " cp /mnt/linuxm.pem /mnt/22Q1"
		}	
		}
		}
			stage ('clone-22Q2') {
			steps {
			dir ('/mnt/22Q2') {
			sh "git clone https://github.com/ronitunale/assignment1.git -b 22Q2"
			sh "chmod -R 777 /mnt/22Q2"
			sh " cp /mnt/linuxm.pem /mnt/22Q2"
			
		}	
		}
		}
			stage ('clone-22Q3') {
			steps {
			dir ('/mnt/22Q3') {
			sh "git clone https://github.com/ronitunale/assignment1.git -b 22Q3"
			sh "chmod -R 777 /mnt/22Q3"
			sh " cp /mnt/linuxm.pem /mnt/22Q3"
			
		}
		}
		}
		stage ('deployment') {
		steps { 
		
		sh "scp -i linuxm.pem /mnt/22Q1/index.html ec2-user@172.31.39.38:/var/www/html"
		sh "scp -i linuxm.pem /mnt/22Q2/index.html ec2-user@172.31.37.146:/var/www/html"
		sh "scp -i linuxm.pem /mnt/22Q3/index.html ec2-user@172.31.43.123:/var/www/html"
		
		
		}
			}
	
	
	}
}
