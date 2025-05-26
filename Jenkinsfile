pipeline{
	agent {
		label 'agent1'
		}
	stages{
		stage("build Docker image"){
			steps{
				sh "docker build -t python:v1"
				}
		}
	}
}