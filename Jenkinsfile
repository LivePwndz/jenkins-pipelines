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
			mail to: 'pwndz172@gmail.com',
				subject: "Jenkins Pipeline Status",
				body: "A pipeline ran and here we are"
		}
		success{
			bat 'echo "Hello there, pipeline success"';
		}
		
		failure{
			bat 'echo "Hello there, pipeline failure"';
		}
	}
}