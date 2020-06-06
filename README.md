# marekbiernacki.com Initial Repository
## Introduction
This is the initial repository for my personal website and portfolio which can be found at [marekbiernacki.com](www.marekbiernacki.com)

## Architecture 
This website is on hosted on a private AWS CodeCommit repository. Each time I push changes to this repository from my machine, it automatically gets deployed through a CodePipeine and CodeBuild process, which pushes the changes to an S3 bucket for the root website domain, which is hosted as a static webpage. Domain registration and routing was done through Route53, while Cloud Network Delivery (CDN) was done through CloudFront. S3 logs of people using the website are saved to an S3 bucket. The architecture of the website is as follows:

![alt tag](https://mb-image-bucket.s3.eu-west-2.amazonaws.com/WebsiteArchitecturev3.svg)