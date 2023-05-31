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
    }
}