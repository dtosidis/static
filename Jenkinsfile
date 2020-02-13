pipeline {
    agent any
    stages {
	stage('Lint HTML') {
	    steps {
			sh 'tidy -q -e *.html'
		}
	}
        stage('Upload to AWS'){
            steps{
			withAWS(region:'eu-central-1', credentials:'aws-static') {
			s3Upload(file:'index.html', bucket:'jenkinsdim', path:'index.html')
		}
            }
        }
    }
}
