pipeline {
    agent any
    stages {
        stage('Submit Stack') {
            steps {
                sh "aws cloudformation create-stack --stack-name s3-01c-cli-stack --template-body 'file://01c-S3.yml' --parameters ParameterKey=BucketNameParam,ParameterValue=test-cf-cli-bucket ParameterKey=EnvironmentName,ParameterValue=test --region 'us-east-1'"
            }
        }
        
    }
}