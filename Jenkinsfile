
Pipeline {
	agent { label 'Jenkins-Agent' }
	tools {
		jdk 'Java17'
		maven 'Maven3'
	}
	stages {
		stage("cleanup workplace") {
			step {
			cleanws()
			}
		}
		stage("checkout from SCM"){
			step {
				git branch: 'main', credentialsid: 'hitgub', url: 'https://github.com/Ashfaque-9x/register-app.git'
				}
		}
		stage("Build Application"){
			step {
  				sh "mvn clean package"
				}	
		}
		stage("Test Application"){
			step {
				sh "mvn test"
				}
		}

