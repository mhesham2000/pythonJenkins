pipeline{
	agent {
		label 'agent1'
		}
	stages{
		stage("build Docker image"){
			steps{
				sh 'docker build -t mhesham2000/pythonhub:${BUILD_NUBMER} .'
				}
					}
		stage("push Docker image"){
			steps{
				sh 'docker push -t mhesham2000/pythonhub:${BUILD_NUBMER} .'
				}
					}

			
		}
	}