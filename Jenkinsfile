pipeline {
	agent any
	
		stages{
			stage('checkout') {
				steps {
					        git branch: 'main', // Specify the 'main' branch to checkout
          url: 'https://github.com/pravinops/day1.git
				}
			}
			stage ('Build Dockerr image') {
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
