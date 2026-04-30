IAM - Identity and Access Management, Global Group
- **root account** is created by default, 
- **Users** are people within your org 
- groups can only contain users not other groups
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