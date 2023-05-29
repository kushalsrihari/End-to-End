pipeline{
	agent any
	stages {
		stage('Sonar Quality Status'){
			agent{
				docker{
					image 'maven'
				}
			}
			steps {
				script{
                    withSonarQubeEnv(credentialsId: 'cicd') {
                        sh 'mvn clean package sonar:sonar'
                        // some block
                    }
				}
			}
		}
	}
}