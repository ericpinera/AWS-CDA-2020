# Demonstrate an Ability to Secure AWS Environments

> How can you control access to the API Gateway in your environment?
>
> Your Answer: API Stages
>
> **Why is this incorrect?**
>
> Is used to host different stages in your API Gateway
>
>
>
> Correct Answer: Cognito User Pools
>
> **Why is this correct?**
>
> AWS documentation: [https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-integrate-with-cognito.htmlControl](https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-integrate-with-cognito.htmlControl) Access to a REST API Using Amazon Cognito User Pools as Authorizer
>
> As an alternative to using IAM roles and policies or Lambda authorizers \(formerly known as custom authorizers\), you can use an Amazon Cognito user pool to control who can access your API in Amazon API Gateway.
>
> To use an Amazon Cognito user pool with your API, you must first create an authorizer of the COGNITO\_USER\_POOLS type and then configure an API method to use that authorizer. After the API is deployed, the client must first sign the user in to the user pool, obtain an identity or access token for the user, and then call the API method with one of the tokens, which are typically set to the request's Authorization header. The API call succeeds only if the required token is supplied and the supplied token is valid, otherwise, the client isn't authorized to make the call because the client did not have credentials that could be authorized.
>
> The identity token is used to authorize API calls based on identity claims of the signed-in user. The access token is used to authorize API calls based on the custom scopes of specified access-protected resources. For more information, see Using Tokens with User Pools and Resource Server and Custom Scopes.Correct 
>
>
>
> Answer: Lambda Authorizers
>
> **Why is this correct?**
>
> AWS documentation: [https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-integrate-with-cognito.htmlControl](https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-integrate-with-cognito.htmlControl) Access to a REST API Using Amazon Cognito User Pools as Authorizer
>
> As an alternative to using IAM roles and policies or Lambda authorizers \(formerly known as custom authorizers\), you can use an Amazon Cognito user pool to control who can access your API in Amazon API Gateway.
>
> To use an Amazon Cognito user pool with your API, you must first create an authorizer of the COGNITO\_USER\_POOLS type and then configure an API method to use that authorizer. After the API is deployed, the client must first sign the user in to the user pool, obtain an identity or access token for the user, and then call the API method with one of the tokens, which are typically set to the request's Authorization header. The API call succeeds only if the required token is supplied and the supplied token is valid, otherwise, the client isn't authorized to make the call because the client did not have credentials that could be authorized.
>
> The identity token is used to authorize API calls based on identity claims of the signed-in user. The access token is used to authorize API calls based on the custom scopes of specified access-protected resources. For more information, see Using Tokens with User Pools and Resource Server and Custom Scopes.



> Server-side encryption is about data encryption at rest. That is, Amazon S3 encrypts your data at the object level as it writes it to disk in its data centers and decrypts it for you when you go to access it. There are a few different options depending on how you choose to manage the encryption keys. One of the options is called 'Server-Side Encryption with Amazon S3-Managed Keys \(SSE-S3\)'. Which of the following best describes how this encryption method works?
>
> Your Answer: You manage the encryption keys and Amazon S3 manages the encryption, as it writes to disk, and decryption, when you access your objects.
>
> **Why is this incorrect?**
>
> Server-side encryption with Amazon S3-managed encryption keys \(SSE-S3\) uses strong multi-factor encryption. Amazon S3 encrypts each object with a unique key. As an additional safeguard, it encrypts the key itself with a master key that it rotates regularly. Amazon S3 server-side encryption uses one of the strongest block ciphers available, 256-bit Advanced Encryption Standard \(AES-256\), to encrypt your data.
>
>
>
> Correct Answer: Each object is encrypted with a unique key employing strong encryption. As an additional safeguard, it encrypts the key itself with a master key that it regularly rotates.
>
> **Why is this correct?**
>
> With this encryption option, Amazon S3 handles all of the encryption/decryption of objects, including the rotation of keys. Other options allow you to manage your own keys if you want, but not the method mentioned in the question.



> You have an Amazon S3 bucket that you use to store objects. You'd like to encrypt some of the new objects you upload to this bucket. What header do you need to use in order to request server-side encryption when using the REST API?
>
> Your Answer: No header is needed
>
> **Why is this incorrect?**
>
> The x-amz-server-side-encryption is required.
>
>
>
> Correct Answer: x-amz-server-side-encryption
>
> **Why is this correct?**
>
> At the time of object creation—that is, when you are uploading a new object or making a copy of an existing object—you can specify if you want Amazon S3 to encrypt your data by adding the x-amz-server-side-encryption header to the request. [https://docs.aws.amazon.com/AmazonS3/latest/dev/SSEUsingRESTAPI.html](https://docs.aws.amazon.com/AmazonS3/latest/dev/SSEUsingRESTAPI.html)



> What two types of encryption can you use with S3?
>
> Correct Answer: Client-Side Encryption
>
> **Why is this correct?**
>
> You can encrypt data client-side and upload the encrypted data to Amazon S3. In this case, you manage the encryption process, the encryption keys, and related tools.
>
> Correct Answer: Server-Side Encryption
>
> **Why is this correct?**
>
> You request Amazon S3 to encrypt your object before saving it on disks in its data centers and decrypt it when you download the objects.



> You have just developed a new application to be deployed on an EC2 instance. The EC2 instance will store data on a separate EBS volume. How would you make sure the data on the EBS volume is encrypted at rest?
>
> Correct Answer: Use KMS to create a customer master key
>
> **Why is this correct?**

> AWS documentation: [https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSEncryption.html](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSEncryption.html)
>
> Amazon EBS encryption offers a simple encryption solution for your EBS volumes without the need to build, maintain, and secure your own key management infrastructure. When you create an encrypted EBS volume and attach it to a supported instance type, the following types of data are encrypted:
>
> Data at rest inside the volume All data moving between the volume and the instance All snapshots created from the volume All volumes created from those snapshots
>
> Amazon EBS encryption uses AWS Key Management Service \(AWS KMS\) customer master keys \(CMKs\) when creating encrypted volumes and any snapshots created from them. A unique AWS-managed CMK is created for you automatically in each region where you store AWS assets. This key is used for Amazon EBS encryption unless you specify a customer-managed CMK that you created separately using AWS KMS.
>
>
>
> Correct Answer: Ensure encryption is enable when creating the volume
>
> **Why is this correct?**
>
> AWS documentation: [https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSEncryption.html](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSEncryption.html)
>
> Amazon EBS encryption offers a simple encryption solution for your EBS volumes without the need to build, maintain, and secure your own key management infrastructure. When you create an encrypted EBS volume and attach it to a supported instance type, the following types of data are encrypted:
>
> Data at rest inside the volume All data moving between the volume and the instance All snapshots created from the volume All volumes created from those snapshots
>
> Amazon EBS encryption uses AWS Key Management Service \(AWS KMS\) customer master keys \(CMKs\) when creating encrypted volumes and any snapshots created from them. A unique AWS-managed CMK is created for you automatically in each region where you store AWS assets. This key is used for Amazon EBS encryption unless you specify a customer-managed CMK that you created separately using AWS KMS.

