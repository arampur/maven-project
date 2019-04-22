pipeline{
	tools {
        maven 'Maven 3.6.1'
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