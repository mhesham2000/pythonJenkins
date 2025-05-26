pipeline{
	agent{
		label "python"
	}
	stages{
		stage("build Docker image"){
			steps{
				sh "docker build -t python:v1"
				}
		}
	}
}