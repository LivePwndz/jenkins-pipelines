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