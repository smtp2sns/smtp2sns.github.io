---
layout: default
title: Home
---

# Welcome to smtp2sns

![Site Logo]({{ '/assets/images/logo.webp' | relative_url }})


**smtp2sns** is a tool that allows you to send SMS messages using an email service. This uses AWS SNS sms service to send SMS.

Example of the email send:
```
From: xxx@xxx.xxx
to: 1xxxxxx@sms.sms
Subject: sms
DATA

SMS to be send.
.
```
And this will send an email to +1xxxxx phone.


## Configuration Guides

- [AWS Configuration](/aws-config/)
- [Mock Service Configuration](/mock-service/)

## Deployment Guides

- [Python Usage](/python/)
- [Docker Usage](/docker/)
- [Docker Compose Usage](/docker-compose/)
- [Helm Chart Usage](/helm-chart/)

## Howto's
- [Howto: test the service](/test/)
