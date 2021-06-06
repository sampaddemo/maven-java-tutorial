pipeline {
	node {
		any
		stages {
			stage('Build') {
				steps {
					git credentialsId: 'git-credential', url: 'https://github.com/sampaddemo/maven-java-tutorial'
					sh ' ./mvnw clean compile
				}


			}

			stage('Test') {
				steps {
					sh './mvnw test
				}

				post {
					always {
						junit '**/target/Test-8.xml'
					}
				}
			}
		}
	}
}
