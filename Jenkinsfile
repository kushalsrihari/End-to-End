@Library('Shared_Jenkins_vars') _

pipeline{
    agent any
    stages{
        stage('Git Checkout'){
            steps{
                gitCheckout(
                    branch: "main",
                    url: "https://github.com/kushalsrihari/End-to-End.git"
                    )
            }
        }
        stage('Unit Test Maven'){
            steps{
                script{
                    mvnTest()
                }
            }
        }
        stage('Integration Test maven'){
            steps{
                script{
                    mvnIntegrationTest()
                }
            }
        }
    }
}