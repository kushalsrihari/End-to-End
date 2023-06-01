pipeline{
    agent any
    stages{
        stage('Git Checkout'){
            steps{
                script{
                    git branch: 'main', url: 'https://github.com/kushalsrihari/End-to-End.git'
                }
            }
        }
    }
}