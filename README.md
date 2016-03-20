

# AWS-IAM-Proxy

Simple proxy to sign requests to AWS infrastructure with a 
IAM signing keys. Can be used to access AWS Elastic Search from
different apps without these needing to implement request signing.

This work is based on the following gist:
https://gist.github.com/nakedible-p/ad95dfb1c16e75af1ad5

# Usage
The preferred way to run this proxy is via docker. The following evironment variables need to be set:

   * AWS_ACCESS_KEY_ID
   * AWS_SECRET_ACCESS_KEY

E.g.:

docker run -it -e AWS_ACCESS_KEY_ID=<aws_access_key> -e AWS_SECRET_ACCESS_KEY=<aws_secret_key> -p 9200:9200 beekeeper/aws-iam-proxy "<aws_search_url>"