pipeline{
	tools {
        maven 'LocalMaven'
    }
    docker {
    image 'maven:LocalMaven-jdk-8'
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