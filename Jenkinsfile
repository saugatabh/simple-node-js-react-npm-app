pipeline {
    agent any
	environment {
        CI = 'true' 
    }
    stages {
        stage('Build') { 
            steps {
                bat 'npm install' 
            }
        }
		stage('Test') { 
            steps {
                bat 'set'
				bat 'echo The following npm  command tests that your simple Node.js/React'
				bat 'echo application renders satisfactorily. This command actually invokes the test'
				bat 'echo runner Jest (https://facebook.github.io/jest/).'
				bat 'npm test'
            }
        }
		stage('Deliver') { 
            steps {
				bat 'echo The following npm  command starts your simple Node.js/React'
				bat 'npm start'				
            }
        }
    }
}