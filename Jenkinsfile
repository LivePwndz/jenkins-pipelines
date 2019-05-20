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
}