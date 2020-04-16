# Demonstrate an Ability to Monitor and Troubleshoot within the AWS Environment

> _**Your team has been asked to migrate the company's on-prem application environment as it stands to Elastic Beanstalk. You conduct research and find no relevant environments in Elastic BeanStalk that would be suitable to host the application. What is the best option?**_
>
> Correct Answer: Use Packer to create a custom platform.
>
> **Why is this correct?**
>
> AWS documentation: h[https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/custom-platforms.html](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/custom-platforms.html) Elastic Beanstalk supports custom platforms. A custom platform is a more advanced customization than a custom image in several ways. A custom platform lets you develop an entire new platform from scratch, customizing the operating system, additional software, and scripts that Elastic Beanstalk runs on platform instances. This flexibility enables you to build a platform for an application that uses a language or other infrastructure software, for which Elastic Beanstalk doesn't provide a managed platform. Compare that to custom images, where you modify an Amazon Machine Image \(AMI\) for use with an existing Elastic Beanstalk platform, and Elastic Beanstalk still provides the platform scripts and controls the platform's software stack. In addition, with custom platforms you use an automated, scripted way to create and maintain your customization, whereas with custom images you make the changes manually over a running instance.
>
> To create a custom platform, you build an AMI from one of the supported operating systems—Ubuntu, RHEL, or Amazon Linux \(see the flavor entry in Platform.yaml File Format for the exact version numbers\)—and add further customizations. You create your own Elastic Beanstalk platform using Packer, which is an open-source tool for creating machine images for many platforms, including AMIs for use with Amazon Elastic Compute Cloud \(Amazon EC2\). An Elastic Beanstalk platform comprises an AMI configured to run a set of software that supports an application, and metadata that can include custom configuration options and default configuration option settings.



> X-Ray metadata:
>
> Correct Answer: Stores key-value pairs of any type that are not searchable
>
> **Why is this correct?**
>
> Correct! This is what X-Ray metadata does.



> AWS X-Ray was recently implemented inside of a service that you work on. Several weeks later, after a new marketing push, that service started seeing a large spike in traffic and you've been tasked with investigating a few issues that have started coming up but when you review the X-Ray data you can't find enough information to draw conclusions so you decide to:
>
> Correct Answer: Update the sampling algorithm to increase the sample rate and instrument X-Ray to collect more pertinent information
>
> **Why is this correct?**
>
> Correct! This is a good way to solve the problem - by customizing the sampling so that you can get more relevant information.



> You define the following S3 bucket policy to grant users access to your bucket, but the S3 bucket policy editor will not allow you to submit it. Why is this policy not working?

> ```text
> {                                                                                                
>   "Id": "Policy1441839160967",                                           
>   "Version": "2012-10-17",                                                    
>   "Statement": [                                                                         
>     {                                                                                              
>      "Sid": "Stmt1441839157568",                                       
>       "Action": [                                                                            
>         "s3:ListBucket"                                                                  
>       ],                                                                                             
>       "Effect": "Allow",                                                                  
>       "Resource": "arn:aws:s3:::linuxacademy.testbucket.2 " 
>    }                                                                                                
>   ]                                                                                                   
> }  
>
> ```

> Correct Answer: A
>
> **Why is this correct?** S3 bucket policies require a Principal be defined
>
> Review the access policy elements here: [https://docs.aws.amazon.com/AmazonS3/latest/dev/access-policy-language-overview.html](https://docs.aws.amazon.com/AmazonS3/latest/dev/access-policy-language-overview.html)







 

