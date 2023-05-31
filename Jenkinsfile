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
                    withSonarQubeEnv(credentialsId: 'cicd1') {
                        sh 'mvn clean package sonar:sonar'
                        // some block
                    }
				}
			}
		}
		stage('Quality Gate status'){
		    steps{
		        script{
		            waitForQualityGate abortPipeline: false, credentialsId: 'cicd1'
		        }
		}
	}
