import hudson.model.*
import groovy.json.JsonSlurper
import groovy.json.JsonBuilder

	pipeline {

		//agent { node { label 'maven' } }
		agent any

		stages {
			stage('Create Pipeline') {
				steps {
					script {
						echo "Hello world! from dummy feature 6"
						String config = readFile file: 'pipeline-config.json'
						def configMap = new JsonSlurper().parseText(config)
						println(new JsonBuilder(configMap).toPrettyString())
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
