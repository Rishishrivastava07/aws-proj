<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Host a Website on Amazon S3

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-host-a-website-on-s3)

**Author:** Rishi Shrivastava  
**Email:** rishishrivastava.91@gmail.com

---

![Image](http://learn.nextwork.org/authentic_lavender_mysterious_beaver/uploads/aws-host-a-website-on-s3_5d4474f9)

---

## Introducing Today's Project!

### Project overview

In this project, I will demonstrate... I'm doing this project to learn...

### Tools and concepts

In this project, I learned how to use Amazon S3 for static website hosting, including bucket creation, region selection, public access settings, bucket policies, ACLs, and understanding website endpoints and permissions to make content publicly accessible.

### Time, challenges, and wins

It took me around 20 minutes to complete the project, including setup, configuration, and testing.

---

## How I Set Up an S3 Bucket

### What I did in this step

In this step, we will open up s3 and then create a storage space inside to start storing website files.

### How long it took to create the bucket

Creating an Amazon S3 bucket takes a few seconds (typically under 10 seconds) and is almost instantaneous once the request is submitted.

### Region selection

The Region I picked for my S3 bucket was ap-south-1. Chosen to minimize latency for India-based users, reduce data transfer costs, and keep data within the same region as other AWS services for better performance and compliance.

### Understanding bucket name uniqueness

It means an Amazon S3 bucket name must be unique across all AWS accounts and all regions worldwide. No two users can have the same bucket name, even if they are in different regions.

![Image](http://learn.nextwork.org/authentic_lavender_mysterious_beaver/uploads/aws-host-a-website-on-s3_ba6d42ad)

---

## Upload Website Files to S3

### What I did in this step

In this step, I will upload the files in inside the s3 bucket.

### Files I uploaded

I uploaded the files to my S3 bucket.

### How the files work together

file is necessary for this project as index.html determines the structure.

![Image](http://learn.nextwork.org/authentic_lavender_mysterious_beaver/uploads/aws-host-a-website-on-s3_a265af88)

---

## Static Website Hosting on S3

### What I did in this step

In this step, I will configure my s3 bucket for static web hosting, and then visit my public website link.

### Understanding website hosting

Website hosting means...Website hosting means storing website files online and making them accessible to users over the internet through a web address.

### How I enabled website hosting

I enabled website hosting by going to the S3 bucket Properties, turning on Static website hosting, and setting index.html as the index document.

### Access Control Lists (ACLs)

An ACL is a legacy permission mechanism in Amazon Web Services that defines who can access an S3 bucket or object and what level of access they have (read/write). ACLs were enabled to allow fine-grained, object-level access control when required.

![Image](http://learn.nextwork.org/authentic_lavender_mysterious_beaver/uploads/aws-host-a-website-on-s3_c22c54c0)

---

## Bucket Endpoints

### Understanding bucket endpoint URLs

A bucket website endpoint URL is the public URL provided by Amazon S3 that allows users to access the static website hosted in the S3 bucket over a web browser.

### What I saw when I tested the endpoint

When I first visited the bucket endpoint URL, I saw access denied error because the objects are not public.

![Image](http://learn.nextwork.org/authentic_lavender_mysterious_beaver/uploads/aws-host-a-website-on-s3_22ce4daf)

---

## Success!

### What I did in this step

In this step, I will make my website files in s3 publicly accessible and see the website live on the internet.

### How I resolved the 403 error

I resolved the 403 Forbidden error by allowing public read access to the S3 bucket and attaching a bucket policy that permits s3:GetObject so the website files can be accessed publicly.

![Image](http://learn.nextwork.org/authentic_lavender_mysterious_beaver/uploads/aws-host-a-website-on-s3_5d4474f9)

---

