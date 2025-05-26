pipeline{
	agent {
		label 'agent1'
		}
	stages{
		stage("build Docker image"){
			steps{
				sh 'docker build -t mhesham2000/pythonhub:${BUILD_NUMBER} .'
				}
					}
		stage("push Docker image"){
			steps{
				sh 'docker push mhesham2000/pythonhub:${BUILD_NUMBER}'

				}
					}

			
		}
	}