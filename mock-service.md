---
layout: default
title: [Feature] Mock Service
permalink: /mock-service/
---

# Mock Service

The mock service disables the operation sns.publish to be able to test without AWS credentials and SNS.

## How to configure

1. On [Docker Usage](/docker/) add an env variable called MOCK_SERVICE="True"
2. Netcat and bash is needed (n

```bash
./test.sh
```

3. execution example:

```bash
$ ./test.sh
220 eccc82e00c5f Python SMTP 1.4.6
250-eccc82e00c5f
250-SIZE 33554432
250-8BITMIME
250-SMTPUTF8
250 HELP
250 OK
250 OK
354 End data with <CR><LF>.<CR><LF>
250 OK: queued as mock:1234
221 Bye
```