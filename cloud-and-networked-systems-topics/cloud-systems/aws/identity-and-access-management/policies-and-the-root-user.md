---
description: Policy types and permission boundary for the root user.
---

# Policies and the root user

The root user is affected only by some policies. Identity based policies are not compatible with the root user. The permissions boundary of the root user cannot be set.

The root user may be designated as principal in a resource-based policy or an Access List. Root user is also member of an account. If that account is a member of the organization in AWS Organizations, the root user is affected by any SCPs tied to the account. 

### Overview of JSON policies

JSON is the format in use for storage and management of policies. 

There are several types of JSON Policies:

* Identity-based Policies - used to set permissions boundaries, to be attached to a user or role. 
* Resource-based Policies - Policy documents to be attached to a resource
* SCPs are JSON - to be attached to an AWS Organizational Unit \(OU\)
* Access-Control Lists attached to a resource but with different syntax. 
* Session policies are assumed with a role or a federated user session. 



* [ ] [How to Create IAM Policies \(Page 456\)](https://docs.aws.amazon.com/IAM/latest/UserGuide/iam-ug.pdf#%5B%7B%22num%22%3A12011%2C%22gen%22%3A0%7D%2C%7B%22name%22%3A%22XYZ%22%7D%2C72%2C394.62%2Cnull%5D)
* [ ] [How to Edit IAM Policies \(Page 482\)](https://docs.aws.amazon.com/IAM/latest/UserGuide/iam-ug.pdf#%5B%7B%22num%22%3A5714%2C%22gen%22%3A0%7D%2C%7B%22name%22%3A%22XYZ%22%7D%2C72%2C175.263%2Cnull%5D)
* [ ] [Validating IAM policies \(Page 462\)](https://docs.aws.amazon.com/IAM/latest/UserGuide/iam-ug.pdf#%5B%7B%22num%22%3A8890%2C%22gen%22%3A0%7D%2C%7B%22name%22%3A%22XYZ%22%7D%2C72%2C365.74%2Cnull%5D)
* [ ] [IAM Access Analyzer policy validation](https://docs.aws.amazon.com/IAM/latest/UserGuide/access-analyzer-policy-validation.html)

### JSON Policy Document Structure

Includes the following elements: 

* Optional policy-wide information at the top of the document
* One of more individual statements

Each statement includes information about a single permission. 

* If there are multiple statements in the policy, AWS applies a logical _OR_ across the statements when evaluating them.
* If there are multiple policies that are in scope of a given request, AWS applies a logical _OR_ across the policies when evaluating them.

![](../../../../.gitbook/assets/image%20%2885%29.png)

Information in a statement is contained within a series of elements:

* **Version**
* **Statement**
* **Sid**
* **Effect**
* **Principal**
* **Action**
* **Resource**
* **Condition** 

More Advanced Policy Elements can be found on:

* [ ] [IAM JSON Policy Elements Reference \(Page 709\)](https://docs.aws.amazon.com/IAM/latest/UserGuide/iam-ug.pdf#%5B%7B%22num%22%3A13764%2C%22gen%22%3A0%7D%2C%7B%22name%22%3A%22XYZ%22%7D%2C72%2C509.625%2Cnull%5D)

