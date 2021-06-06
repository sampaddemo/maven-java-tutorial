pipeline {
	node {
		any
		stages {
			stage('Build') {
				steps {
					git credentialsId: 'git-credential', url: 'https://github.com/sampaddemo/maven-java-tutorial'
					sh ' ./mvn clean compile
				}


			}

			stage('Test') {
				steps {
					sh './mvn test
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
