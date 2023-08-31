pipeline{
	agent any
	environment{
		PATH="$PATH:/opt/apache-maven-3.6.3/bin"
	}
	stages{
		stage('GetCode'){
			steps{
				git branch: 'main',
				url: 'https://github.com/koranneudit/jenkins.git'
			}
		}
			
		stage('Code Deploy'){
			steps{
				sshagent(['Tomcat-Server']) {
				sh 'scp -o StrictHostkeychecking=no target/01-Maven-Web-App.war ec2-user@3.111.51.11:/home/ec2-user/apache-tomcat-9.0.68/webapps'
				}
			}	
		}
		
	}	
}
