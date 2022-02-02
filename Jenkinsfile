pipeline {
    agent any
    stages {
	    stage('Checkout') {
	    	steps {
				    git branch: 'master',
				    credentialsId: '08c74917-d1e2-4ad6-a53b-047ce9b8f0be',
				    url: 'https://github.com/rupeshpanchal21/dev-repo.git'
    			}
    		}
		stage('build') {
			steps {
					 bat 'mvn install'
				}
			}
			stage('test') {
				steps {
					 bat 'mvn test'
				}
			}
		}
    }