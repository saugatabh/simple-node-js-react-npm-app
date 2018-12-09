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
                bat 'simple-node-js-react-npm-app/jenkins/scripts/test.sh'
            }
        }
    }
}