//

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
				sh 'docker build -t mhesham2000/pythonhub:${BUILD_NUMBER} .'
				}
					}
		stage("push Docker image"){
			steps{
				sh 'docker login -u ${DOCKER_USER} -p ${DOCKER_PASSWORD}'
				sh 'docker push mhesham2000/pythonhub:${BUILD_NUMBER}'

				}
					}

			
		}
	}

//

// script //


node('agent1'){

	withCredentials([
		string(credentialsId: 'dockerhub-user', variable: 'DOCKER_USER'),
		string(credentialsId: 'dockerhub-passsword', variable: 'DOCKER_PASSWORD')

			]){
			
		 stage('Build Docker image') {
           		    sh "docker build -t mhesham2000/pythonhub:${env.BUILD_NUMBER} ."
   					     }

    	   	 stage('Push Docker image') {
        		    sh "docker login -u ${DOCKER_USER} -p ${DOCKER_PASSWORD}"
          		    sh "docker push mhesham2000/pythonhub:${env.BUILD_NUMBER}"
      						  }
		  		}
}