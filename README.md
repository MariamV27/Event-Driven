# Event-Driven Image Processing Pipeline with AWS Lambda and S3

### This project demonstrates how to build an automated, event-driven image processing pipeline using AWS Lambda and S3. When an image is uploaded to a source S3 bucket, an AWS Lambda function is triggered, which processes the image by pixelating it into five different resolutions: 8x8, 16x16, 32x32, 48x48, and 64x64, using the Pillow (PIL) library. The processed images are then stored in a processed S3 bucket. This project leverages a fully serverless architecture, ensuring scalability and cost-effectiveness.

## Project Solution:

## Stage 1: Create the S3 Buckets
Bucket 1: amc-image-pixelater-source
Bucket 2: amc-image-pixelater-processed

## Stage 2: Develop the Lambda Function Code:


 - Create a folder named my_lambda_deployment.
   
   Move into that folder (cd my_lambda_deployment).
   
   Create a folder called lambda.
   
   Move into that folder (cd lambda).
   
   Create a file called lambda_function.py and paste in the code for the
   pixelator Lambda function.
   
   Download this file PIL Package into that folder.
   
   Run unzip
   Pillow-9.0.1-cp39-cp39-manylinux_2_17_x86_64.manylinux2014_x86_64.whl
   and then rm
   Pillow-9.0.1-cp39-cp39-manylinux_2_17_x86_64.manylinux2014_x86_64.whl.
   These are the Pillow module files required for image manipulation in
   Python 3.9 (which the lambda function will be using).
   
   From the same folder, run zip -r ../my-deployment-package.zip . which
   will create a lambda function zip, containing all these files in the
   parent directory.
   
   This zip will be the same zip which is linked below, so if you have
   any issues with the lambda function, you can use the one that's
   pre-created.

## Stage 3 - Create and Configure the Lambda Function
## Stage 4 - Test and Monitor