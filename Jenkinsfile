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
		
		
	}	
}
