pipeline{
    agent any
    stages {
        
        stage("Checkout scm")
{
  steps{
          checkout scm
}
}

        
        stage('submit stack') {
            steps {
                bat "aws cloudformation create-stack --stack-name MyStack --template-body file://ec2cft.yaml --region 'us-east-1'"
            }
        }

    }
}
