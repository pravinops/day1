pipeline {
	agent any
	
		stages{
			stage('checkout') {
				steps {
					git 'https://github.com/pravinops/day1.git'
				}
			}
			stage ('Build Docker image') {
				steps {
					script {
						def imageName = 'pravinraj:latest'
						sh "docker build -t ${imageName} . "
					}
				}
			}
			stage ('Push Docker Image') {
				steps {
					script {
						def imageName = 'pravinraj:latest'
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
