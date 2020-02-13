pipeline {
    agent any
    stages {
        stage('Build'){
            steps{
			withAWS(region:'eu-central-1', credentials:'aws-static') {
			s3Upload(file:'index.html', bucket:'jenkinsdim', path:'index.html')
            }
        }
    }
}
