# Task 15: CloudFront Distribution for S3 Static Website

## Objective
To configure Amazon CloudFront as a Content Delivery Network (CDN) for an S3 static website in order to improve performance and enable global content distribution.

## Services Used
- Amazon S3
- Amazon CloudFront
- IAM (for permissions)

## Architecture
User → CloudFront (CDN) → S3 Bucket (Static Website Hosting)

CloudFront caches website content at edge locations worldwide, reducing latency and improving website loading speed.

## Implementation Steps

### Step 1: Create S3 Bucket
- Created an S3 bucket
- Enabled Static Website Hosting
- Uploaded index.html file
- Made bucket objects publicly accessible (or configured proper policy)

### Step 2: Create CloudFront Distribution
- Opened CloudFront console
- Clicked "Create distribution"
- Selected S3 bucket as Origin
- Default cache behavior kept as default
- Viewer protocol policy: Redirect HTTP to HTTPS
- Created distribution

### Step 3: Access Website via CloudFront
- Waited for distribution status to become "Deployed"
- Copied CloudFront Domain Name
- Accessed website using CloudFront URL

## Configuration Details
- Origin: S3 bucket
- Default root object: index.html
- Price class: Default
- Distribution state: Enabled

## Proof
- Screenshot 1: S3 static website hosting enabled
- Screenshot 2: CloudFront distribution showing deployed status and domain name

## Result
The static website hosted on S3 is successfully delivered through CloudFront CDN, providing faster and globally distributed content access.
