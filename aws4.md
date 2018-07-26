Loadbalncer :

loadbalncer means it will balnce the load,we have a server at time we will many user hit the server means server performance go to down, over  come this issue aws was introduced loadbalncer.

First we have to create the loadbalncer after that select that server to that loadbalncer then, loadbalncer given one url for that both server. Once config that it will automatically balnce the load.

![load](https://github.com/malli2221/ops/blob/master/imgt/load1.png)

server`1:

![load](https://github.com/malli2221/ops/blob/master/imgt/load2.png)

server2:

![load](https://github.com/malli2221/ops/blob/master/imgt/load3.png)

create the loadbalncer:

![load](https://github.com/malli2221/ops/blob/master/imgt/load5.png)

loadbancer url:

![load](https://github.com/malli2221/ops/blob/master/imgt/load6.png)

**![load](https://github.com/malli2221/ops/blob/master/imgt/load8.png)**

**Auto scaling :**

Aws autoscaling: why we need autoscaling if server performance will increse that we need create other server manually but in aws is provided autoscaling once we configure that it will automatically create onther server. For this we need take server backup first using that AMI we configure the autoscaling if server performance reach to 85% means it will create the server, when server performance decrease means it will stop the server based our conditions.



**S3 Bucket :**

Amazon S3 is cloud storage for the internet. To upload your data (photos, videos, documents etc.), you first create a bucket in one of the AWS Regions. You can then upload any number of objects to the bucket. In terms of implementation, buckets and objects are resources, and Amazon S3 provides APIs for you to manage them.

An Amazon S3 bucket name is globally unique, regardless of the AWS Region in which you create the bucket. You specify the name at the time you create the bucket

**Creating a Bucket**

Amazon S3 provides APIs for creating and managing buckets. By default, you can create up to 100 buckets in each of your AWS accounts. When you create a bucket, you provide a name and the AWS Region where you want to create the bucket, we have given unique name for that bucket.

About Permissions

You can use your AWS account root credentials to create a bucket and perform any other Amazon S3 operation. However, AWS recommends not using the root credentials of your AWS account to make requests such as to create a bucket. Instead, create an IAM user, and grant that user full access (users by default have no permissions). We refer to these users as administrator users. You can use the administrator user credentials, instead of the root credentials of your account, to interact with AWS and perform tasks, such as create a bucket, create users, and grant them permissions.

Accessing a Bucket

You can access your bucket using the Amazon S3 console. Using the console UI, you can perform almost all bucket operations without having to write any code.

If you access a bucket programmatically, note that Amazon S3 supports RESTful architecture in which your buckets and objects are resources, each with a resource URI that uniquely identifies the resource.

**Bucket Configuration Options :**

Amazon S3 supports various options for you to configure your bucket. For example, you can configure your bucket for website hosting, add configuration to manage lifecycle of objects in the bucket, and configure the bucket to log all access to the bucket. Amazon S3 supports subresources for you to store, and manage the bucket configuration information. That is, using the Amazon S3 API, you can create and manage these subresources. You can also use the console or the AWS SDKs.

| Subresource | Description |
| --- | --- |
| _location_ | When you create a bucket, you specify the AWS Region where you want Amazon S3 to create the bucket. Amazon S3 stores this information in the location subresource and provides an API for you to retrieve this information. |
| _policy_ and _ACL_ (access control list) | All your resources (such as buckets and objects) are private by default. Amazon S3 supports both bucket policy and access control list (ACL) options for you to grant and manage bucket-level permissions. Amazon S3 stores the permission information in the _policy_ and _acl_ subresources.   |
| _cors_ (cross-origin resource sharing) | You can configure your bucket to allow cross-origin requests.   |
| _website_ | You can configure your bucket for static website hosting. Amazon S3 stores this configuration by creating a _website_ subresource.   |
| _logging_ | Logging enables you to track requests for access to your bucket. Each access log record provides details about a single access request, such as the requester, bucket name, request time, request action, response status, and error code, if any. Access log information can be useful in security and access audits. It can also help you learn about your customer base and understand your Amazon S3 bill.     |
| _event notification_ | You can enable your bucket to send you notifications of specified bucket events.   |
| _versioning_ | Versioning helps you recover accidental overwrites and deletes. We recommend versioning as a best practice to recover objects from being deleted or overwritten by mistake.   |
| _lifecycle_ | You can define lifecycle rules for objects in your bucket that have a well-defined lifecycle. For example, you can define a rule to archive objects one year after creation, or delete an object 10 years after creation.   |
| cross-region replication | Cross-region replication is the automatic, asynchronous copying of objects across buckets in different AWS Regions. For more information, |
| _tagging_ | You can add cost allocation tags to your bucket to categorize and track your AWS costs. Amazon S3 provides the _tagging_ subresource to store and manage tags on a bucket. Using tags you apply to your bucket, AWS generates a cost allocation report with usage and costs aggregated by your tags. |
| _requestPayment_ | By default, the AWS account that creates the bucket (the bucket owner) pays for downloads from the bucket. Using this subresource, the bucket owner can specify that the person requesting the download will be charged for the download. Amazon S3 provides an API for you to manage this subresource. . |
| _transfer acceleration_ | Transfer Acceleration enables fast, easy, and secure transfers of files over long distances between your client and an S3 bucket. Transfer Acceleration takes advantage of Amazon CloudFront&#39;s globally distributed edge locations. |
