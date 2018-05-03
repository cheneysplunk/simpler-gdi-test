# Create CloudTrail
Testing x y z
1. Sign in to the AWS Management Console and open the [Cloudtrail console](https://console.aws.amazon.com/). 
2. Choose the region where you want the trail to be created.
3. Choose **Get Started Now**.
4. On the **Create Trail** page, for **Trail name**, type a name for your trail. For more information, see [CloudTrail Trail Naming Requirements](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-trail-naming-requirements.html).
5. For **Apply trail to all regions**, choose **Yes** to receive log files from all regions. This is the default and recommended setting. If you choose **No**, the trail logs files only from the region in which you create the trail.
6. For **Management events**, for **Read/Write events**, choose if you want your trail to log **All**, **Read-only**, **Write-only**, or **None**, and then choose **Save**. By default, trails log all management events. For more information, see [Management Events](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/logging-management-and-data-events-with-cloudtrail.html#logging-management-events).
7. For **Storage location**, for **Create a new S3 bucket**, choose **Yes** to create a bucket. When you create a bucket, CloudTrail creates and applies the required bucket policies.

Note: If you choose No, choose an existing S3 bucket. The bucket policy must grant CloudTrail permission to write to it. For information about manually editing the bucket policy, see [Amazon S3 Bucket Policy for CloudTrail](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/create-s3-bucket-policy-for-cloudtrail.html).

8. For **S3 bucket**, type a name for the bucket you want to designate for log file storage. The name must be globally unique. For more information, see [Amazon S3 Bucket Naming Requirements](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-s3-bucket-naming-requirements.html).

9. (Optional) Configure advanced settings for your trail. 
	* For **Storage location**, choose **Advanced**.
	* In the Log file prefix field, type a prefix for your Amazon S3 bucket. THe prefix is an addition to the URL for an Amazon S3 object that creates a folder-like organization in your bucket. The location where your log files will be stored appears under the text field.
	* For **Encrypt log files**,  choose **Yes** if you want AWS KMS to encrypt your log files.
	* For **Create a new KMS key**, choose **Yes** to create a key or **No** to use an existing one.
	* If you chose Yes, type an alias in the KMS key field. CloudTrail encrypts your log files with the key and adds the policy for you. 

10. Choose **Create**.
11. The new trail appears on the Trails page. The Trails page shows the trails in your account from all regions. In about 15 minutes, CloudTrail publishes log files that show the AWS API calls made in your account. You can see the log files in the S3 bucket that you specified.
