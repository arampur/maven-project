pipeline{
	tools {
        maven 'LocalMaven'
    }
    
    environment {
    registry = "arampur89/tomcatwebapp"
    registryCredential = 'dockerhub'
 	}
	agent any
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