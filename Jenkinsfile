pipeline {
	agent any
	
		stages{
			stage('checkout') {
				steps {
					git branch: 'main', url: 'https://github.com/pravinops/day1.git'
				}
			}
			stage ('Build Docker image') {
				steps {
					scripts {
						def imageName = 'pravin:latest'
						sh "docker tag  ${imageName}  pravin23devops/${image.name} . "
					}
				}
			}
			stage ('Push Docker Image') {
				steps {
					scripts {
						def imageName = 'pravin:latest'
						sh "docker push ${imageName} "
					}
				}
			}
			stage ('Push Docker Image') {
				steps {
					scripts {
						def imageName = 'pravin:latest'
						sh "docker push ${imageName} "
					}
				}
			}
		}
		post {
			success {
				echo "success"
			}
			failure {
				echo "problem"
			}
		}
	}
