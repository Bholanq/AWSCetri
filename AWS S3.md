**Amazon S3 (Simple Storage Service)** is a **scalable object storage service** from Amazon Web Services used to store and retrieve **any amount of data from anywhere**.

S3 = **unlimited /infinitely scaling storage for files (objects)** in the cloud

![[Pasted image 20260504152450.png]]

# Buckets
- Directories/Containers to store **objects**/files
- **Regional**
- Objects - Can be:
    - Images
    - Videos
    - PDFs
    - Backups
    - Logs

Each object =  
**Data + Metadata + Key (name/path)**

### Key
- Unique identifier of object inside bucket

![[Pasted image 20260504152707.png]]

# Objects 
#### There's no concept of directories within S3 buckets, we just have keys which looks like paths with directories.


Key = **prefix+object name**

![[Pasted image 20260504153306.png]]

![[Pasted image 20260504153420.png]]

# [[ S3 - Security]]

- user-based
- resource-based
	- bucket policies 
	- object access control list (ACL)
	- BUCKET ACL
![[Pasted image 20260504155337.png]]

![[Pasted image 20260504182007.png]]
# [[S3 Bucket Policies ]]
- JSON based policies 
- Same as general policies 
- ![[Pasted image 20260504155656.png]]

External User - Bucket Policy 
IAM user - IAM Policy 
EC2 Instance - IAM Roles
Cross account access - Bucket Policy 
![[Pasted image 20260504160115.png]]


# [[S3 Static Website Hosting ]]

S3 can host websites and have them accessible on the internet 

URL: depending on the region
![[Pasted image 20260504162503.png]]
### Always make sure to allow public reads.


# [[S3 Versioning]] 

### Has to enabled at the Bucket Level
- Not enabled by default
- any file present before the enabling versioning will have the version null
- ![[Pasted image 20260504164815.png]]
ADV:
- Rollback and version control

![[Pasted image 20260504164206.png]]

## Deleting a version is permanent and cannot be undone except for null versions

#### When we delete a null version of an obj it creates a "delete marker" version.
- This "Delete Marker" version can't be used
We can restore the original object by deleting the "Delete Marker" version.
![[Pasted image 20260504165641.png]]


# [[S3 - Replication (CRR & SRR)]]

## ASYNC

![[Pasted image 20260504170510.png]]

**SRR is close to live but still async**

- Only new object are replicated after replications is enabled, use S3 BATCH REPLICATION FOR OLD OBJECTS
- ![[Pasted image 20260504171635.png]]
- ![[Pasted image 20260504170917.png]]
- Can replicate delete markers only, permanent deletion does not cause replication.
- No chaining of replicates

# [[S3- Storage Classes]]


