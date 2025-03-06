---
layout: default
title: Helm Chart Usage
permalink: /helm-chart/
---

# Helm Chart Usage

## How to use smtp2sns with Helm

1. Add the Helm repository:

```bash
helm repo add smtp2sns https://smtp2sns.github.io/smtp2sns
```

1. create a secret in kubernetes to store AWS credentials:

```bash
kubectl create secret generic aws-credentials \
    --from-literal=AWS_ACCESS_KEY_ID='xxxx' \
    --from-literal=AWS_SECRET_ACCESS_KEY='yyyy'

```

2. create a values.yaml file with the `topic` and the `region`:

```yaml
app:
  region: us-west-1
  # add topic arn value
  topic: arn:aws:sns:us-west-1:xxxxx:MyTopic
  # mock service (do not use in production)
  #mock: "true"  
  secret:
    name: aws-credentials
```

3. execute the helm chart

```bash
helm install smtp2sns smtp2sns/smtp2sns -f values.yaml
```

4. [optional] execute helm chart from this repo:

```bash
helm install smtp2sns ./charts/smtp2sns -f values.yaml
```

5. then you can send emails using this configuration (`host:port`) without credentials:

```
smtp2sns:1025
```
