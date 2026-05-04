IAM - Identity and Access Management, Global Group
- **root account** is created by default, 
- **Users** are people within your org 
- **groups can only contain users not other groups**
- A user doesn't have to belong to a group, and can also belong to multiple groups
![[Pasted image 20260430073723.png]]

# IAM Permissions
 - Users or Groups are assigned JSON documents called **policies**
 - These policies define the permissions of the users
 - In AWS, we follow the **least privilege principal**: don't give more permissions required than a user needs

An IAM user has a different login from a IAM root account. 
Along with different Acoount IDs
We can see "IAM user" Specified 
![[Pasted image 20260430080218.png]]

# Multi-Session Support
Allows us to access multiple accounts on the same browser. 
- The accounts are either root and users or user and user accounts.

# IAM Policies Inheritance 
![[Pasted image 20260430082047.png]]

- Group-wise
- Inline
# IAM Policy Structure

JSON Document 
![[Pasted image 20260430082500.png|618]]

eg. IAMReadOnlyAccess - Allows the user to look at the list of users

### The user will inherit all the policies of all the groups it is in + inline policies 
![[Pasted image 20260430092440.png|601]]

We can also create custom policies. 

# IAM Password Policy 
- Set up min password length
- Specific characters
- Allow IAM users to change their own passwords
- Pass word expiration 

# MFA - Multi Factor Auth
- must protect the root device 
- MFA = password you know + security device you own 

#### Virtual MFA Devices
- Google Auth 
- Authy 
#### U2F (Universal 2nd Factor)
- YubiKey
#### Hardware Key Fob 
- Gemato

# IAM Roles for services
- Some AWS services need to perform actions on our behalf 
- to do so we will need assign permissions to AWS Services with IAM Roles
- ie. giving entities permissions to perform stuff on aws
- common roles:
	- EC2 instance
	- Lambda Function roles
	- Roles for CloudFormation
	![[Pasted image 20260430130633.png]]
We use something called an EC2 Instance basically a Virtual Server and for this server to use AWS we need to provide it it with IAM Role permissions.

# IAM Security Tools 
### IAM Credentials Report(account-level)
In AWS IAM, **credentials in the IAM Credentials Report** refer to the different ways a user can authenticate (prove their identity) to access AWS services.

### IAM Access Advisor(user-level)
- Show the permissions granted to a user and when those services were last used
- You can use this information to revise your policies

# Best Practices 
![[Pasted image 20260430150007.png|512]]

**[[Policies vs Roles]]**
