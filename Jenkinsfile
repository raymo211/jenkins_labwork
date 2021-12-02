pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/raymo211/jenkins_labwork.git']]])
            }
        }
	stage('Build'){
	    steps{
		git branch: 'main', url: 'https://github.com/raymo211/jenkins_labwork.git'
		sh 'python3 test2.py'	
            }
	}
    }
}
