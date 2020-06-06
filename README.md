# Personal Website and portfolio
## Introduction
This is the initial repository for my personal website which can be found at [marekbiernacki.com](http://www.marekbiernacki.com). The website is a simple template which I have adapted to host my portfolio, it is likely to adapt and change over time. 

## Architecture 

![alt tag](https://mb-image-bucket.s3.eu-west-2.amazonaws.com/WebsiteArchitecturev3.svg)

This website is hosted on a private AWS CodeCommit repository. Each time I push changes to this repository from my machine, it automatically gets deployed through a CodePipeine and CodeBuild process. This automatically pushed the changes to an S3 bucket for the root domain website, which is hosted as a static webpage. Domain registration and routing was done through Route53, while Cloud Network Delivery (CDN) was done through CloudFront. S3 logs of people using the website are saved to an S3 bucket. 