# CloudFormation python custom resource for blocking public S3 buckets for an entire account

The custom resource in this repository enables you to use the newly added S3 feature for [blocking the creation of public S3 buckets in an AWS account](https://aws.amazon.com/blogs/aws/amazon-s3-block-public-access-another-layer-of-protection-for-your-accounts-and-buckets/).

This custom resource allows you to configure all features for blocking the creation of public S3 buckets. 
The parameters when "True" will configure the following:

ACLBlockPublicParameter - Block public access to buckets and objects granted through NEW access control lists (ACLs)

ACLIgnorePublicParameter - Block public access to buckets and objects granted through ANY access control lists (ACLs)

BucketPolicyBlockPublicParameter - Block public access to buckets and objects granted through NEW public bucket or access point policies

BucketPolicyRestrictPublicParameter - Block public and cross-account access to buckets and objects through ANY public bucket or access point policies

For use with Stacksets use overrides to configure different settings for various accounts under a single stackset.
