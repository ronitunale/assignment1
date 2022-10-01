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
			sh "rm -rf *"
			sh "git clone https://github.com/ronitunale/assignment1.git -b 22Q1"
			sh "chmod -R 777 /mnt/22Q1"
			sh " cp /mnt/linuxm.pem /mnt/22Q1/"
			sh "chmod 400 /mnt/22Q1/linuxm.pem"
			sh "chmod -R 777 /mnt/22Q1/"
		}	
		}
		}
			stage ('clone-22Q2') {
			steps {
			dir ('/mnt/22Q2') {
			sh "rm -rf *"
			sh "git clone https://github.com/ronitunale/assignment1.git -b 22Q2"
			sh "chmod -R 777 /mnt/22Q2"
			sh " cp /mnt/linuxm.pem /mnt/22Q2/"
			sh "chmod 400 /mnt/22Q2/linuxm.pem"
			sh "chmod -R 777 /mnt/22Q2/"
			
		}	
		}
		}
			stage ('clone-22Q3') {
			steps {
			dir ('/mnt/22Q3') {
			sh "rm -rf * "
			sh "git clone https://github.com/ronitunale/assignment1.git -b 22Q3"
			sh "chmod -R 777 /mnt/22Q3"
			sh " cp /mnt/linuxm.pem /mnt/22Q3/"
			sh "chmod 400 /mnt/22Q3/linuxm.pem"
			sh "chmod -R 777 /mnt/22Q3/"
			
		}
		}
		}
		stage ('copy-key') {
		steps { 
		sh " cp /mnt/linuxm.pem /mnt/22Q1/assignment1/"
		sh "chmod 400 /mnt/22Q1/assignment1/linuxm.pem"
		sh " cp /mnt/linuxm.pem /mnt/22Q2/assignment1/"
		sh "chmod 400 /mnt/22Q2/assignment1/linuxm.pem"
		sh " cp /mnt/linuxm.pem /mnt/22Q3/assignment1/"
		sh "chmod 400 /mnt/22Q3/assignment1/linuxm.pem"
		}
		}
		
		stage ('deployment') {
		steps {
		sh "scp -i /mnt/22Q1/assignment1/linuxm.pem /mnt/22Q1/assignment1/index.html ec2-user@172.31.38.85:/var/www/html/"
		sh "scp -i /mnt/22Q2/assignment1/linuxm.pem /mnt/22Q2/assignment1/index.html ec2-user@172.31.34.224:/var/www/html/"
		sh "scp -i /mnt/22Q3/assignment1/linuxm.pem /mnt/22Q3/assignment1/index.html ec2-user@172.31.47.12:/var/www/html/"
		
	
		
		}
			}
	
	
	}
}
