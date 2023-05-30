<h2>Step-by-step guide</h2>
<ol>
    <li>Prepare an image: Select an image that you would like to upload and have it ready on your local machine. Ensure that the image is in a supported format such as JPEG or PNG.</li>
    <li>Upload the image to the S3 bucket:</li>
    <ul>
        <li><strong>AWS Management Console:</strong></li>
        <li>Go to the Amazon S3 console.</li>
        <li>Select the S3 bucket that was created by your CloudFormation stack (check the ImageBucketName output in the CloudFormation stack's Outputs tab).</li>
        <li>Click the "Upload" button and follow the prompts to select and upload your image file.</li>
        <li><strong>AWS CLI:</strong></li>
        <li>Open a command-line interface or terminal.</li>
        <li>Use the following AWS CLI command to upload the image to the S3 bucket, replacing &lt;your-bucket-name&gt; with the actual bucket name:</li>
    </ul>
</ol>

<code>aws s3 cp &lt;path-to-your-image-file&gt; s3://&lt;your-bucket-name&gt;</code>

<p>To deploy the CloudFormation stack, you can use the AWS Management Console, AWS CLI, or AWS SDKs. Make sure you have the necessary permissions to create the required resources. When deploying the stack, provide a value for the BucketName parameter to specify the name of the S3 bucket that will be created for image uploads.</p>

<p>After the stack is successfully deployed, you can upload images to the S3 bucket, and the Lambda function will automatically trigger and perform image recognition using Amazon Rekognition. The detected labels will be printed in the Lambda function's logs.</p>


<!-- Add more image tags here -->
