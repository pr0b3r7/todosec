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
* Session



