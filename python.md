---
layout: default
title: Python Usage
permalink: /python/
---

# Python Usage

## How to use smtp2sns 

1. Set the environment variables

```bash
export AWS_REGION=us-west-1
export TOPIC_ARN=arn:aws:sns:us-west-1:account-id:topic-name
export AWS_ACCESS_KEY_ID=xxxx
export AWS_SECRET_ACCESS_KEY=yyyy
```

2. Install dependencies

```bash
cd smtp2sns
pip install -r requirements.txt
```

3. Run program:

```bash
python smtp_to_sns.py
2025-03-06 17:46:25,267 - mail.log - INFO - ('172.22.0.1', 41904) sender: sender@example.com
2025-03-06 17:46:25,267 - mail.log - INFO - ('172.22.0.1', 41904) >> b'RCPT TO:<1234567890@sms.sms>'
2025-03-06 17:46:25,268 - SNSHandler - INFO - Accepted recipient: 1234567890@sms.sms
2025-03-06 17:46:25,268 - mail.log - INFO - ('172.22.0.1', 41904) recip: 1234567890@sms.sms
2025-03-06 17:46:25,268 - mail.log - INFO - ('172.22.0.1', 41904) >> b'DATA'
2025-03-06 17:46:25,268 - SNSHandler - INFO - Received message from: sender@example.com
2025-03-06 17:46:25,268 - SNSHandler - INFO - Recipients: ['1234567890@sms.sms']
2025-03-06 17:46:25,269 - SNSHandler - INFO - Extracted phone number: +1234567890
2025-03-06 17:46:25,269 - SNSHandler - INFO - Attempting to send SMS...
2025-03-06 17:46:25,269 - SNSHandler - INFO - MOCK_SERVICE: simulation
2025-03-06 17:46:25,269 - SNSHandler - INFO - SMS sent to +1234567890: Message ID: mock:1234
```

4. then you can send emails using `localhost:1025` without credentials [Howto: test the service](/test/)