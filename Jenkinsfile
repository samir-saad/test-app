import hudson.model.*

	pipeline {

		//agent { node { label 'maven' } }
		agent any

		stages {
			stage('Create Pipeline') {
				steps {
					script {
						echo "Hello world!"
					}
				}
			}
		}
		post('Finalize') {
			always {
				script {
					echo "Done!"
				}
			}
		}
	}
