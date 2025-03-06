---
layout: default
title: AWS SNS configuration
permalink: /aws-config/
---

# Helm Chart Usage

## Create a SNS topic to send SMS

1. Create a SNS to send sms obtain the `topic_arn` in a specific AWS Region. (like: `arn:aws:sns:us-west-1:account-id:topic-name`)
2. Keep both Arn and AWS Region 


## Create an IAM User

1. create an AWS user in IAM that has the following permissions: `sns:Publish` to the specific topic_arn
2. create AWS credentials to access to this user. 
3. Save both AWS_ACCESS_KEY_ID and AWS_SECRET_ACCESS_KEY


Policy Example:
```json
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Action": "sns:Publish",
            "Resource": "arn:aws:sns:region:account-id:topic-name"
        }
    ]
}
```
