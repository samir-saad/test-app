import hudson.model.*

	pipeline {

		//agent { node { label 'maven' } }
		agent any

		stages {
			stage('Create Pipeline') {
				steps {
					script {
						echo "Hello world! from dummy feature 3"
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
