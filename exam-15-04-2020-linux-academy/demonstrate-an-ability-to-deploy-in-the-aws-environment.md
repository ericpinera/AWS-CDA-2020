# Demonstrate an Ability to Deploy in the AWS Environment

> Company B has many users updating the same table. At times it is not uncommon for multiple users to update the same item and attribute of an item at the same time. If user A calls an item in a table to update an attribute at the same time as user B and user B updates the table first, what can we deploy in DynamoDB to ensure User A is not updating an item that was updated since User A's table read?
>
> Your Answer: Atomic Counters
>
> **Why is this incorrect?**
>
> A conditional write is required. With a conditional write, an operation succeeds only if the item attributes meet one or more expected conditions; otherwise it returns an error.
>
> Correct Answer: Conditional Writes
>
> **Why is this correct?**
>
> With a conditional write, an operation succeeds only if the item attributes meet one or more expected conditions; otherwise it returns an error.



> Which of the following is the right sequence that gets called in CodeDeploy when you use Lambda hooks in an EC2/On-Premise Deployment?
>
> Correct Answer: Application Stop-Before Install-After Install-Application Start
>
> **Why is this correct?**
>
> AWS documentation:[https://docs.aws.amazon.com/codedeploy/latest/userguide/reference-appspec-file-structure-hooks.html\#reference-appspec-file-structure-hooks-run-order](https://docs.aws.amazon.com/codedeploy/latest/userguide/reference-appspec-file-structure-hooks.html#reference-appspec-file-structure-hooks-run-order) In an in-place deployment, including the rollback of an in-place deployment, event hooks are run in the following order:
>
> Note An AWS Lambda hook is one Lambda function specified with a string on a new line after the name of the lifecycle event. Each hook is executed once per deployment. Following are descriptions of the lifecycle events where you can run a hook during an Amazon ECS deployment.
>
> BeforeInstall – Use to run tasks before the replacement task set is created. One target group is associated with the original task set. If an optional test listener is specified, it is associated with the original task set. A rollback is not possible at this point. AfterInstall – Use to run tasks after the replacement task set is created and one of the target groups is associated with it. If an optional test listener is specified, it is associated with the original task set. The results of a hook function at this lifecycle event can trigger a rollback. AfterAllowTestTraffic – Use to run tasks after the test listener serves traffic to the replacement task set. The results of a hook function at this point can trigger a rollback. BeforeAllowTraffic – Use to run tasks after the second target group is associated with the replacement task set, but before traffic is shifted to the replacement task set. The results of a hook function at this lifecycle event can trigger a rollback. AfterAllowTraffic – Use to run tasks after the second target group serves traffic to the replacement task set. The results of a hook function at this lifecycle event can trigger a rollback. Run Order of Hooks in an Amazon ECS Deployment
>
> In an Amazon ECS deployment, event hooks run in the following order:
>
> For in-place deployments, the six hooks related to blocking and allowing traffic apply only if you specify a Classic Load Balancer, Application Load Balancer, or Network Load Balancer from Elastic Load Balancing in the deployment group.Note The Start, DownloadBundle, Install, and End events in the deployment cannot be scripted, which is why they appear in gray in this diagram. However, you can edit the 'files' section of the AppSpec file to specify what's installed during the Install event.



> You run an ad-supported photo sharing website using S3 to serve photos to visitors of your site. At some point you find out that other sites have been linking to the photos on your site, causing loss to your business. What is an effective method to mitigate this?
>
> Your Answer: Use CloudFront distributions for static content.
>
> **Why is this incorrect?**
>
> CloudFront on its own doesn't prevent unauthorized access and requires you to add a whole new layer to your stack \(which may make sense anyway\). You can serve private content, but you'd have to use signed URLs or similar mechanism. Here are the docs: [http://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/PrivateContent.html](http://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/PrivateContent.html)
>
> Correct Answer: Remove public read access and use signed URLs with expiry dates.
>
> **Why is this correct?**
>
> This solves the issue, but does require you to modify your website. Your website already uses S3, so it doesn't require a lot of changes. See the docs for details: [http://docs.aws.amazon.com/AmazonS3/latest/dev/ShareObjectPreSignedURL.html](http://docs.aws.amazon.com/AmazonS3/latest/dev/ShareObjectPreSignedURL.html)



> Your application utilizes Amazon S3 reduced redundancy storage and you have configured the s3:ReducedRedundancyLostObject notification on your Amazon S3 Bucket. What services might you use to create a "distributed" platform that replaces lost RRS objects on Amazon S3 automatically?
>
> Correct Answer: SNS with SQS subscription endpoint with a worker instance
>
> **Why is this correct?**
>
> The s3:ReducedRedundancyLostObject can send a notification to a specified SNS topic. Using that topic and SQS as a subscription end point allowing the lost object message to wait inside of a queue until a worker instance retrieves the message from the queue and recreates the original object that was lost.



> You are having trouble maintaining session states on some of your applications that are using an Elastic Load Balancer\(ELB\). To overcome this problem which of the following is the recommended method by AWS to try and rectify the issues that you are having?
>
> Your Answer: Use ElastiCache, which is a web service that makes it easy to set up, manage, and scale a distributed in-memory cache environment in the cloud.
>
> **Why is this incorrect?**
>
> The best method for maintaining application session state is to use the sticky session feature \(also known as session affinity\),
>
> Correct Answer: Use the sticky session feature \(also known as session affinity\), which enables the load balancer to bind a user's session to a specific instance. This ensures that all requests from the user during the session are sent to the same instance.
>
> **Why is this correct?**
>
> The best method for maintaining application session state is to use the sticky session feature \(also known as session affinity\),



> CodeBuild projects have configuration settings that determine things like:
>
> Your Answer: A
>
> **Why is this incorrect?**
>
> Sorry! This isn't part of the configuration, this might be an "Action" within CodePipeline though.Your Answer: D
>
> **Why is this incorrect?**
>
> Sorry! This sort of approval process could actually be defined inside of the CodePipeline service, but not CodeBuild.
>
> Correct Answer: Where the project's source code is located
>
> **Why is this correct?**
>
> Correct! This is one part of what the configuration settings might include.
>
> Correct Answer: Where to store the output of the build
>
> **Why is this correct?**
>
> Correct! This is one part of what the configuration settings might include.





