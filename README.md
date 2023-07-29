# S3_static_website_host

AWS S3 stands for Amazon Simple Storage Service. It is a cloud-based storage service that can scale to an enormous size and provide high performance, availability, reliability, and security. It is a very cost-effective and secure replacement for your on-premises data center. The data is stored on cloud servers can be accessed through other web applications and websites globally.

Apart from data storage functionality, the AWS S3 bucket provides a remarkable feature of static website hosting over it.

A website that doesn’t involve server-side communication is called a static website. In this guide, we will discuss a step-by-step procedure for hosting a static website on the AWS S3 bucket.


## Step1 : 
First create an S3 bucket and give your website DNS as its name.

DNS name : example.com
S3 bucket name : sample.example.com

## Step2 : 
Now enable static website hosting for that bucket. For that got to your bucket --> Properties --> "Static website hosting" --> set it to enabled --> set "Index document" as index.html. Then save it and we will get a URL for our site.

![image](https://github.com/Blesson02/S3_static_website_host/assets/108075329/7fb9532a-ade0-4c7c-b598-a3d77f19f9f4)

`http://sample.example.com.s3-website-us-east-1.amazonaws.com`

## Step3 : 
Now Upload a sample html website contents to our bucket. (For this example i use "https://www.tooplate.com/" site ).
Download the site to your local machine and upload it to S3 bucket.

## Step4 :
Now our website shows 403 Forbidden error. That's because by default S3 bucket is in private mode. So we need to open it to public and also need to add one bucket policy to access random users.
