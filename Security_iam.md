<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Cloud Security with AWS IAM

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-security-iam)

**Author:** Rishi Shrivastava  
**Email:** rishishrivastava.91@gmail.com

---

![Image](http://learn.nextwork.org/authentic_lavender_mysterious_beaver/uploads/aws-security-iam_1c864649)

---

## Introducing Today's Project!

### Project overview

I demonstrate how IAM users, groups, and policies work in AWS, along with how authentication and authorization are implemented using AWS services. This project also provides hands-on insight into cloud security fundamentals and best practices for managing access and permissions securely.

### Tools and concepts

Services I used were IAM groups, users, policies, EC2, account alias.

### Project reflection

This project took me approximately 30 mins.

---

## Tags

### What I did in this step

In this step, I will have launched two instances to increase computing power.

### Understanding tags

Tags in EC2 are key–value labels attached to resources like instances, volumes, and snapshots to help identify and manage them easily. They are useful for organizing resources by purpose (such as Dev, Test, or Prod), tracking costs in billing by project or team, applying access control using IAM policies, and enabling automation through scripts and AWS services. Tags do not affect how an EC2 instance works, but they provide clarity, control, and efficient management, especially when handling multiple resources in a large AWS environment.

### My tag configuration

The tag i have used are production for the prod instance and development for the dev instance.

![Image](http://learn.nextwork.org/authentic_lavender_mysterious_beaver/uploads/aws-security-iam_2e0e5a5d)

---

## IAM Policies

### What I did in this step

In this step, I will create an IAM policy to access the development instance.

### Understanding IAM policies

IAM policies define permissions in AWS by specifying what actions are allowed or denied on which resources. They are used to control access securely by attaching policies to users, groups, or roles, ensuring that only authorized entities can perform specific operations on AWS services, following the principle of least privilege.

### The policy I set up

For this project, I’ve set up a policy using JSON.

### Policy effect

This policy allows some actions (like starting, stopping, and describing EC2 instances) for instances tagged with "Env = development" while denying the ability to create or delete tags for all instances.

### Understanding Effect, Action, and Resource

In an IAM JSON policy, Effect specifies whether a permission is Allowed or Denied, Action defines the specific AWS operations that are permitted or restricted (such as starting or stopping an EC2 instance), and Resource indicates the AWS resources on which those actions can be performed, together forming the rule that controls access in AWS.

---

## My JSON Policy

![Image](http://learn.nextwork.org/authentic_lavender_mysterious_beaver/uploads/aws-security-iam_1c864649)

---

## Account Alias

### What I did in this step

Simplify user login to your AWS account using an Account Alias.

### Understanding account aliases

An Account Alias is a human-readable name you assign to your AWS account that replaces the numeric account ID in the AWS Management Console sign-in URL, making it easier to remember and share for login purposes, while not affecting security, permissions, or account functionality in any way.

### Setting up my account alias

Creating an account alias took me less than 10 seconds.

![Image](http://learn.nextwork.org/authentic_lavender_mysterious_beaver/uploads/aws-security-iam_0eb4439b)

---

## IAM Users and User Groups

### What I did in this step

Setting up a dedicated IAM group for all NextWork interns, so you can manage all interns' permissions from one place.
Setting up a dedicated IAM user for your new intern, so they have a way to log in.

### Understanding user groups

IAM user groups are collections of IAM users that simplify permission management by allowing you to assign IAM policies to a group once and automatically apply those permissions to all users in the group, making access control consistent, scalable, and easier to manage in AWS.

### Attaching policies to user groups

Attaching a policy to a user group means that all users in that group automatically inherit the permissions defined in the policy, including both existing members and any users added in the future. This approach centralizes access control, ensures consistent permissions across users with the same role, reduces manual configuration, and makes permission management easier and more scalable. Any change to the policy at the group level is instantly reflected for all group members, which aligns with AWS IAM best practices and supports the principle of least privilege.

### Understanding IAM users

IAM users are individual identities created within AWS Identity and Access Management (IAM) that represent a person or an application interacting with AWS. Each IAM user has unique security credentials (such as a username, password, or access keys) and is granted specific permissions through IAM policies to securely access AWS resources. IAM users help enforce controlled access, accountability, and least-privilege security within an AWS account.

---

## Logging in as an IAM User

### Sharing sign-in details

The two ways to share a new IAM user’s sign-in details are by providing the AWS Management Console sign-in URL along with the username and a temporary password, or by sharing the access key ID and secret access key when the user needs programmatic access.

### Observations from the IAM user dashboard

Once I logged in as my IAM user, I noticed some of your dashboard panels are showing Access denied already.

![Image](http://learn.nextwork.org/authentic_lavender_mysterious_beaver/uploads/aws-security-iam_6f2ab446)

---

## Testing IAM Policies

### What I did in this step

Log into AWS using the intern's IAM user.
Test the intern's access to your production and development instance.

### Testing policy actions

I tested my two instances by stopping both the instances production instance showed error because of the policy defined earlier. and the second instance stopped beacause the user was authorized to in the policy.

### Stopping the production instance

A banner tells us we've failed to stop this instance. The banner tells us it's because we're not authorized! We don't have permission to stop any instance with the production tag.

![Image](http://learn.nextwork.org/authentic_lavender_mysterious_beaver/uploads/aws-security-iam_0e7a9d6a)

### Stopping the development instance

It resulted in error, because the user is not authorized to do so.

![Image](http://learn.nextwork.org/authentic_lavender_mysterious_beaver/uploads/aws-security-iam_1811801c)

---

## IAM Policy Simulator

### Understanding the IAM Policy Simulator

### How I used the simulator

---

---
