pipeline{
	tools {
        maven 'LocalMaven'
    }
    
	agent {
		docker { image 'node:7-alpine' }
	}
	stages
	{
		stage('Build'){
			steps{
				sh 'mvn clean package'
				sh "docker build . -t tomcatwebapp:${env.BUILD_ID}"
			}
		}
	}
}