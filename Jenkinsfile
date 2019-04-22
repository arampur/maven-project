pipeline{
	tools {
        maven 'LocalMaven'
    }
	agent any
	stages
	{
		stage('Build'){
			steps{
				sh 'mvn clean package'
			}
		}
	}
}