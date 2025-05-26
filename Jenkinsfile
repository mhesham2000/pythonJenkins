pipeline{
	agent any
	stages{
		stage("build Docker image"){
			steps{
				sh "docker build -t python:v1"
				}
		}
	}
}