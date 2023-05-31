pipeline{
    agent any
    stages{
        stage('Git Checkout'){
            steps{
                scripts{
                    git branch: 'main', url: 'https://github.com/kushalsrihari/End-to-End.git'
                }
            }
        }
    }
}