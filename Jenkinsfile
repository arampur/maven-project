pipeline{
	tools {
        maven 'LocalMaven'
        docker 'maven:3-alpine'
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