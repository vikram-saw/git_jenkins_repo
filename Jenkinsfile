pipeline {
    agent any
    stages {
        stage('Submit Stack') {
            steps {
                sh "aws cloudformation create-stack --stack-name test-s3-bucket-pipeline --template-body 'file://01c-S3.yml' --parameters ParameterKey=BucketNameParam,ParameterValue=jenkins-cf-cli-bucket ParameterKey=EnvironmentName,ParameterValue=$EnvironmentName --region 'us-east-1'"
            }
        }
        
    }
}