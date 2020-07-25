---
date: 2020-07-24T20:14:55-07:00
title: Debug-Ssl-Flask-Setup
tags: System SSL Flask Python
---

# Debug-Ssl-Flask-Setup

Had issues with Slack verifying the webhook and the reason turned out issues with SSL. when digging further, came to know that the SSL Chain is not set up properly. 

`/etc/letsencrypt/live/example.com/fullchain.pem instead of /etc/letsencrypt/live/example.com/cert.pem`

