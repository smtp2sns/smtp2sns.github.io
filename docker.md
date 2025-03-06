---
layout: default
title: Docker Usage
permalink: /docker/
---

# Docker Usage

## How to use smtp2sns with Docker


```bash
docker run -d --rm -p 1025:1025 -e TOPIC_ARN=arn:xxx -e AWS_REGION=us-west-1 -e AWS_ACCESS_KEY_ID=xxxx -e AWS_SECRET_ACCESS_KEY=yyyy ghcr.io/smtp2sns/smtp2sns
```

then you can send emails using `localhost:1025` without credentials