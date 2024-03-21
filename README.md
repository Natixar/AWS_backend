# Natixar Cloud Infrastructure

We are proud to be completely transparent regarding how we store and manage user data. Every aspect of our AWS cloud 
infrastructure is described in this repository, in a hierarchy of cloudformation templates. 

## Deployment

The deployment is automated, except for the databases. The GitHub files are synchronized to S3, where they can be 
compiled into one big ``aws cloudformation`` cloud resources configuration script. The synchronization from GitHub
relies on a dedicated AWS IAM User called ``automation_github_S3_sync`` who belongs to a role named ``role_S3_sync``
that has the following privileges:

* s3:PutObject
* s3:GetObject
* s3:ListBucket

  
