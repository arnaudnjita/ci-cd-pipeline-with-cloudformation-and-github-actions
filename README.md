# ci-cd-pipeline-with-cloudformation-and-github-actions

1. Create a Github repository named "ci-cd-pipeline-with-cloudformation-and-github-actions"
2. Clone the repository to your local machine
3. Create a yaml file in the repo named "single-tier-app.yaml"
4. Add the following code to the yaml file
<!-- 
Resources:
  S3Bucket:
    Type: AWS::S3::Bucket
    Properties:
      BucketName: my-static1-websit2e-bucket
      AccessControl: PublicRead
      WebsiteConfiguration:
        IndexDocument: index.html
  BucketPolicy:
    Type: AWS::S3::BucketPolicy
    Properties:
      Bucket: !Ref S3Bucket
      PolicyDocument:
        Statement:
        - Sid: PublicReadGetObject
          Effect: Allow
          Principal: '*'
          Action: s3:GetObject
          Resource: !Join ['', ['arn:aws:s3:::', !Ref S3Bucket, '/*']]
-->
5. Copy the "index.html" file into the working local repository and edit the names "Relindis" in the file with yours if you wish
6. Login to your AWS console and grant an IAM user the "AWSCloudFormationFullAccess" permission 
7. Open your Github repository in the browser and navigate to the settings tab
   In the settings tab scroll down to the "Secrets and variables" section in the left panel and click on "Actions"
   Here we are going to create secret variables to store our access key id and secret access key of our IAM user
   Click on new repository secret 
   In the name input field enter the variable name AWS_ACCESS_KEY_ID and in the secret input field paste the AWS_ACCESS_KEY_ID of the IAM user
   Create another new repository secret 
   In the name input field enter the variable name AWS_SECRET_ACCESS_KEY and in the secret input field paste the AWS_SECRET_ACCESS_KEY of the IAM user
8. 


