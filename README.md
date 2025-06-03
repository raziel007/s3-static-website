#S3 Static Website

This folder helps you set up a public static website on AWS using S3 and Terraform.

What You'll Learn
How to host a basic website on S3
How to make your site public
How to use Terraform for it
What You Need

AWS CLI: https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html

Terraform: https://developer.hashicorp.com/terraform/downloads

Steps

1. Add your website files
Inside this folder, create a file called index.html and add some basic HTML like:

<h1>Hello from BuildWithStu!</h1>
You can also create an error.html if you want.

2. Run Terraform

Set up your AWS credentials:
aws configure
-Access Key
-Secret Key

Then run these commands in this folder:

terraform init
terraform plan
terraform apply
Say yes to confirm.

3. Find your website URL
Once it’s created, your website will be available at a URL like:

http://your-bucket-name.s3-website-us-east-1.amazonaws.com
You can also find it in the AWS Console under the bucket’s “Properties” tab, under “Static website hosting.”

To Delete the Website
Run:

terraform destroy

Notes
Make sure your bucket name is unique
You can always change the content in index.html and run terraform apply again
