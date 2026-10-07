# static-website-s3-hosting
# Static Website Hosting on AWS S3

Hosted a responsive static portfolio website using Amazon S3 static website hosting feature with high availability and low cost.

## Services Used
S3, IAM, S3 Bucket Policy

## Architecture
User -> S3 Bucket URL -> index.html -> CSS/JS files

## Deployment Steps
1. Created S3 bucket: vinayaka-portfolio-2024 (unique name)
2. Disabled Block all public access (required for static hosting)
3. Enabled Static website hosting: Properties -> Static website hosting -> Enable
4. Set Index document: index.html, Error document: error.html
5. Created simple website files:
   - index.html (Home page)
   - style.css (Styling)
   - script.js (Optional)
   - error.html (404 page)
6. Uploaded files to S3 bucket
7. Added Bucket Policy to allow public read:
{
  "Version": "2012-10-17",
  "Statement": [{
    "Effect": "Allow",
    "Principal": "*",
    "Action": "s3:GetObject",
    "Resource": "arn:aws:s3:::vinayaka-portfolio-2024/*"
  }]
}
8. Tested website using S3 Endpoint URL: http://vinayaka-portfolio-2024.s3-website.ap-south-1.amazonaws.com
9. Optional: Added versioning and cost optimization

## Files in this Repo
- index.html - Main portfolio page
- error.html - Custom error page

## Key Learnings
S3 hosting, Bucket Policies, Public access, Static website endpoints, Cost optimization (S3 is cheaper than EC2 for static sites)

## Live Demo
Endpoint: your-bucket-name.s3-website.ap-south-1.amazonaws.com

## Author
Vinayaka Garapatti | Linux | CCNA | AWS | Bangalore
