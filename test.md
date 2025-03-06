---
layout: default
title: Helm Chart Usage
permalink: /test/
---

# Testing

## How to use test script to simulate a client

1. There is a test script to localhost:1025 to test the smtp server. 
2. Netcat and bash is needed (nc)

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