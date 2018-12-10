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
				bat 'start npm start'
			}
        }
		stage('Kill') { 
            steps {
				bat 'echo ... will wait for 25 secs and then kill'
				timeout 15 > NUL
				bat 'taskkill /F /IM node.exe'
            }
        }
		
    }
}