pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                bat 'set'
				bat '''
                    echo "Multiline shell steps works too"
                    dir
                '''
            }
        }
		stage('deplo') {
			steps {
				input "Continue to deployment?"
				bat 'echo Deployment done.'
			}
		}
    }
	
	post{
		always{
			bat 'echo "Hello there, pipeline done"';
		}
		success{
			bat 'echo "Hello there, pipeline success"';
		}
		
		failure{
			bat 'echo "Hello there, pipeline failure"';
		}
	}
}