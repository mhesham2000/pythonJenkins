pipeline{
	agent {
		label 'agent1'
		}
	stages{
		stage("build Docker image"){
			steps{
				sh 'docker build mhesham2000/pythonhub:${BUILD_NUBMER} .'
				}
					}
		stage("push Docker image"){
			steps{
				sh 'docker push mhesham2000/pythonhub:${BUILD_NUMBER}'

				}
					}

			
		}
	}