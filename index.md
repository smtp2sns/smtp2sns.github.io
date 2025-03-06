# Welcome to smtp2sns

**smtp2sns** is a tool that allows you to send SMS messages using an email service. This uses AWS SNS sms service to send SMS.

## How It Works
1. Send an email to a specific address.
2. The email is converted into an SMS using AWS SNS sms service.
3. The SMS is delivered to the recipient's phone.
