pipeline{
agent any
stages{
      stage('deploy to S3'){
          steps{
              sh 'aws s3 cp git-github/index.html s3://nikhiltestwebsite.com'
              sh 'aws s3api put-object-acl --bucket nikhiltestwebsite.com --key index.html --acl public-read'
              sh 'aws s3 cp git-github/error.html s3://nikhiltestwebsite.com'
              sh 'aws s3api put-object-acl --bucket nikhiltestwebsite.com --key error.html --acl public-read'
          }
      }
  }
}  
