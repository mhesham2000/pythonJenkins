pipeline{
	agent{
		label "pythonApp"
	}
	stages{
		stage("build Docker image"){
			steps{
				sh "docker build -t python:v1"
				}
		}
	}
}