@Library('libx')_
def mydocker = new org.lab3.docker()


pipeline{
	agent {
		label 'agent1'
		}

	environment{

		DOCKER_USER = credentials('dockerhub-user')
		DOCKER_PASSWORD = credentials('dockerhub-password')
		
	}
	
	stages{
		stage("build Docker image"){
			steps{
				script{
					
					mydocker.buildDockerImage("mhesham2000/pythonhub" , BUILD_NUMBER)
		}
	}
}
		stage("push Docker image"){
			steps{
				script{
					mydocker.login(DOCKER_USER , DOCKER_PASSWORD)
					mydocker.dockerPush("mhesham2000/pythonhub", BUILD_NUMBER )
					
					}
				}
			}

			
	}
}
