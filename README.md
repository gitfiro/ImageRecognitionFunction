# ImageRecognitionFunction
CloudFormation template that you can use to build a Serverless Image Recognition application using AWS Lambda, Amazon Rekognition, and Amazon S3:

Here's a step-by-step guide on how to use your deployed Serverless Image Recognition application:

Prepare an image: Select an image that you would like to upload and have it ready on your local machine. Ensure that the image is in a supported format such as JPEG or PNG.

Upload the image to the S3 bucket: There are multiple ways to upload the image to the S3 bucket. Let's go through two common methods:

AWS Management Console:

Go to the Amazon S3 console.
Select the S3 bucket that was created by your CloudFormation stack (check the ImageBucketName output in the CloudFormation stack's Outputs tab).
Click the "Upload" button and follow the prompts to select and upload your image file.
AWS CLI:

Open a command-line interface or terminal.
Use the following AWS CLI command to upload the image to the S3 bucket, replacing <your-bucket-name> with the actual bucket name:

aws s3 cp <path-to-your-image-file> s3://<your-bucket-name>

To deploy the CloudFormation stack, you can use the AWS Management Console, AWS CLI, or AWS SDKs. Make sure you have the necessary permissions to create the required resources. When deploying the stack, provide a value for the BucketName parameter to specify the name of the S3 bucket that will be created for image uploads.

After the stack is successfully deployed, you can upload images to the S3 bucket, and the Lambda function will automatically trigger and perform image recognition using Amazon Rekognition. The detected labels will be printed in the Lambda function's logs.

