---
layout: default
title: Docker-Compose Usage
permalink: /docker-compose/
---

# Docker-Compose Usage

## How to use smtp2sns with docker-

1. Add the following `.env` file by the `docker-compose.yml` file:

```bash
vi .env
TOPIC_ARN=arn:aws:sns:us-west-1:account-id:topic-name
AWS_REGION=us-west-1
AWS_ACCESS_KEY_ID=xxxx
AWS_SECRET_ACCESS_KEY=yyyy
```
2. Then use docker command

```bash
docker compose up -d
```


then you can send emails using `localhost:1025` without credentials. [Howto: test the service](/test/)

## Add Mock feature

1. Add the following `.env` file by the `docker-compose.yml` file:

```bash
MOCK_SERVICE=True
```

2. Then use docker command

```bash
docker compose up -d
```

The service will be mocked, don't use in production.[Mock Service Feature](/mock-service/)